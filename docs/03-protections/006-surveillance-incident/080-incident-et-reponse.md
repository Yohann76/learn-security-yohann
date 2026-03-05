# Incident et réponse

La cybersécurité n'est pas seulement une question de prévention - les incidents se produisent même dans les organisations les mieux protégées. La capacité à détecter, analyser et répondre efficacement aux incidents de sécurité est devenue une compétence essentielle pour les professionnels de la cybersécurité. Ce chapitre explore les principes fondamentaux de la gestion des incidents et de la réponse, les méthodologies établies, et les meilleures pratiques pour limiter les dommages et restaurer les opérations normales.

## 1. Définition d'un Incident de Sécurité

Un **incident de sécurité** est un événement qui compromet ou menace de compromettre la confidentialité, l'intégrité ou la disponibilité des systèmes d'information ou des données d'une organisation. 

*   **Exemples d'incidents** :
  *   Violations de données
  *   Intrusions dans les systèmes
  *   Attaques par déni de service (DoS/DDoS)
  *   Infections par malware (ransomware, virus, etc.)
  *   Compromission de comptes utilisateurs
  *   Exfiltration de données sensibles
  *   Utilisation non autorisée de ressources informatiques

## 2. Cycle de Vie de la Réponse aux Incidents

Le NIST (National Institute of Standards and Technology) définit un **cycle de vie de réponse aux incidents** en quatre phases principales :

### 2.1 Préparation

La phase de **préparation** établit les fondements d'une réponse efficace aux incidents avant qu'ils ne surviennent.

*   **Éléments clés** :
  *   Développement de politiques et procédures de réponse
  *   Constitution d'une équipe de réponse aux incidents (CSIRT)
  *   Formation et sensibilisation du personnel
  *   Mise en place d'outils et de technologies
  *   Établissement de communications et coordinations
  *   Création et maintenance de plans de réponse aux incidents
  *   Préparation d'un environnement d'analyse forensique

### 2.2 Détection et Analyse

La phase de **détection et analyse** implique l'identification des incidents potentiels et leur analyse pour déterminer leur nature, leur portée et leur impact.

*   **Processus de détection** :
  *   Surveillance des alertes des systèmes de sécurité (SIEM, IDS, EDR)
  *   Analyse des journaux et du trafic réseau
  *   Signalements internes ou externes
  *   Détection d'anomalies comportementales

*   **Analyse préliminaire** :
  *   Évaluation de l'impact et de la criticité
  *   Classification de l'incident
  *   Détermination des ressources nécessaires
  *   Documentation des observations initiales
  *   Établissement d'une chronologie des événements

### 2.3 Confinement, Éradication et Rétablissement

Cette phase comprend trois étapes critiques pour répondre à l'incident et restaurer les opérations normales.

*   **Confinement** :
  *   Isolation des systèmes compromis
  *   Blocage des adresses IP malveillantes
  *   Restriction des accès réseau
  *   Création d'images forensiques des systèmes affectés
  *   Mise en œuvre de stratégies de confinement à court et long terme

*   **Éradication** :
  *   Identification et suppression des malwares et backdoors
  *   Correction des vulnérabilités exploitées
  *   Réinitialisation des mots de passe compromis
  *   Nettoyage complet de tous les systèmes affectés

*   **Rétablissement** :
  *   Restauration sécurisée des systèmes et des données
  *   Validation de la sécurité des systèmes restaurés
  *   Retour progressif à la production
  *   Surveillance accrue des systèmes restaurés

### 2.4 Activités Post-Incident

Les **activités post-incident** visent à tirer des enseignements de l'incident pour améliorer la posture de sécurité globale.

*   **Éléments essentiels** :
  *   Organisation de réunions de retour d'expérience
  *   Documentation complète de l'incident
  *   Analyse des causes profondes
  *   Identification des améliorations nécessaires
  *   Mise à jour des plans de réponse aux incidents
  *   Partage d'informations avec les parties prenantes concernées

## 3. Équipe de Réponse aux Incidents

Une **équipe de réponse aux incidents** (CSIRT - Computer Security Incident Response Team) est essentielle pour coordonner et exécuter les activités de réponse.

*   **Composition typique** :
  *   **Responsable d'équipe** : Coordonne les efforts et communique avec la direction
  *   **Analystes de sécurité** : Détectent et analysent les incidents
  *   **Experts en forensique numérique** : Collectent et analysent les preuves
  *   **Administrateurs systèmes et réseaux** : Aident au confinement et au rétablissement
  *   **Experts en communication** : Gèrent les communications internes et externes
  *   **Conseillers juridiques** : Assurent la conformité avec les obligations légales
  *   **Représentants des ressources humaines** : Gèrent les incidents impliquant le personnel

## 4. Outils et Technologies de Réponse aux Incidents

Plusieurs catégories d'outils sont essentielles pour une réponse efficace aux incidents :

*   **Détection et surveillance** :
  *   Systèmes de gestion des événements et des informations de sécurité (SIEM)
    * **Splunk Enterprise Security** : Analyse avancée de logs et détection de menaces
    * **IBM QRadar** : Corrélation d'événements en temps réel
  *   Systèmes de détection/prévention d'intrusion (IDS/IPS)
    *  **Suricata :** Moteur IDS/IPS open source haute performance
    *  **Snort :** IDS/IPS open source largement utilisé
    *  **Cisco Firepower :** Solution commerciale complète
    *  **Palo Alto Networks IDS :** Fonctionnalités intégrées aux pare-feux
    *  **Darktrace :** Utilise l'IA pour détecter les anomalies réseau
  *   Solutions de détection et réponse des endpoints (EDR)
    *  **CrowdStrike Falcon :** Plateforme cloud avec IA et machine learning
    *  **SentinelOne :** Protection autonome avec réponse automatisée
    *  **Microsoft Defender for Endpoint :** Intégré à l'écosystème Windows
    *  **Carbon Black (VMware) :** Analyse comportementale avancée
    *  **Sophos Intercept X :** Protection contre les menaces avancées
  *   Analyses comportementales et détection d'anomalies
    *  **Vectra AI :** Détection basée sur l'IA pour les menaces réseau
    *  **ExtraHop Reveal(x) :** Analyse du trafic réseau en temps réel
    *  **Darktrace Enterprise Immune System :** Modélisation du comportement normal
    *  **Cisco Stealthwatch :** Analyse des flux réseau et détection d'anomalies
    *  **Awake Security :** Analyse comportementale avancée du réseau
*   **Investigation et forensique** :
  *   Outils d'acquisition d'images disque
    *  **FTK Imager :** Création d'images forensiques et récupération de données
    *  **EnCase Forensic :** Solution complète d'analyse forensique
    *  **SANS SIFT Workstation :** Distribution Linux avec outils forensiques
    *  **dd/dcfldd :** Utilitaires Linux pour création d'images bit à bit
    *  **X-Ways Forensics :** Outil avancé pour l'analyse forensique
  *   Analyseurs de mémoire volatile
    *  **Volatility Framework :** Outil open source pour l'analyse de mémoire RAM
    *  **Rekall :** Framework d'analyse de mémoire dérivé de Volatility
    *  **Redline (FireEye) :** Analyse de mémoire et détection de malware
    *  **Magnet RAM Capture :** Outil simple de capture mémoire
    *  **WinPmem/DumpIt :** Utilitaires légers pour acquisition de mémoire
  *   Outils d'analyse de malware
    *  **Cuckoo Sandbox :** Environnement d'analyse automatisé open source
    *  **VirusTotal :** Service d'analyse de fichiers suspects en ligne
    *  **IDA Pro/Ghidra :** Désassembleurs pour l'analyse de code malveillant
    *  **REMnux :** Distribution Linux spécialisée dans l'analyse de malware
    *  **YARA :** Outil de reconnaissance de patterns pour identifier les malwares
  *   Logiciels d'analyse de logs et de trafic réseau
    *  **Wireshark :** Analyseur de protocoles réseau open source
    *  **NetworkMiner :** Outil forensique réseau pour capture de paquets
    *  **Zeek (Bro) :** Framework d'analyse et surveillance du trafic réseau
    *  **Moloch (Arkime) :** Système de capture et indexation de paquets à grande échelle
    *  **Graylog :** Gestion et analyse centralisée des logs
*   **Gestion et orchestration** :
  *   Plateformes de gestion des incidents
    *  **IBM Resilient :** Plateforme de gestion des incidents et réponse
    *  **TheHive :** Solution open source de gestion des incidents
    *  **RTIR (Request Tracker for Incident Response) :** Système open source
    *  **D3 Security :** Solution spécialisée pour les équipes IR
    *  **ServiceNow SecOps :** Gestion des flux de travail de sécurité
  *   Solutions SOAR (Security Orchestration, Automation and Response)
    *  **Palo Alto Networks Cortex XSOAR :** Automatisation des réponses
    *  **Splunk Phantom :** Orchestration et automatisation des tâches
    *  **Rapid7 InsightConnect :** Workflows personnalisables d'automatisation
    *  **Swimlane :** Plateforme d'automatisation de la sécurité
    *  **Siemplify (Google) :** Orchestration cloud de la sécurité
  *   Systèmes de ticketing et de suivi
    *  **Jira Service Management :** Suivi et gestion des incidents
    *  **RT (Request Tracker) :** Système de ticketing flexible open source
    *  **OTRS/((OTRS)) Community Edition :** Plateforme de gestion d'incidents
    *  **Freshservice :** Solution cloud de gestion des services IT
    *  **ManageEngine ServiceDesk Plus :** Outil complet de gestion des incidents
    *  **Gitlab/Github :** Solutions intégré dans le developpement 

## 5. Documentation et Preuves

La **documentation** joue un rôle crucial dans la réponse aux incidents, en particulier si des poursuites judiciaires sont envisagées.

*   **Bonnes pratiques** :
  *   Maintenir une chaîne de possession rigoureuse pour les preuves
    *  Assure l'admissibilité des preuves en justice
    *  Démontre que les preuves n'ont pas été altérées ou compromises
    *  Permet de prouver qui a eu accès aux preuves et quand
    *  Utilisation de formulaires standardisés de transfert
    *  Documentation photographique si nécessaire
    *  Registre des accès aux zones de stockage sécurisées
  *   **Documenter toutes les actions entreprises avec horodatage**
    *  Utilisation d'un système de journalisation centralisé
    *  Capture d'écran des actions importantes
    *  Notes détaillées des procédures suivies
    *  Enregistrement des commandes exécutées
    *  Documentation des résultats obtenus
    *  Rapport des anomalies rencontrées
  *   **Capturer des copies forensiques des systèmes compromis**
    *  Création d'images bit-à-bit
    *  Vérification des sommes de contrôle
    *  Documentation du matériel utilisé
    *  Capture de la mémoire volatile (RAM)
    *  Sauvegarde des configurations système
    *  Préservation des métadonnées
  *   **Préserver les logs et autres preuves volatiles**
    *  Capture immédiate des logs système
    *  Sauvegarde des journaux d'applications
    *  Export des logs de sécurité
    *  Copie des logs réseau
    *  Archivage des traces d'audit
    *  Documentation des processus en cours
  *   **Utiliser des outils de hachage pour valider l'intégrité des preuves**
    *  Calcul des hashes MD5
    *  Vérification SHA-256
    *  Documentation des valeurs de hachage
    *  Double validation avec différents algorithmes
    *  Stockage sécurisé des valeurs de hachage
    *  Vérification périodique de l'intégrité
  *   **Stocker les preuves de manière sécurisée**
    *  Utilisation de coffres-forts numériques
    *  Chiffrement des données sensibles
    *  Contrôle d'accès strict
    *  Surveillance environnementale
    *  Copies de sauvegarde sécurisées
    *  Procédures de destruction sécurisée

## 6. Communication en Situation de Crise

La **communication** pendant un incident est essentielle pour coordonner la réponse et gérer les attentes.

*   **Éléments clés** :
  *   **Plan de communication d'incident préétabli**
    * Définition des rôles et responsabilités
    * Procédures de notification par niveau de gravité
    * Modèles de communication préparés
    * Liste des contacts d'urgence
    * Processus de validation des communications
  *   **Canaux de communication sécurisés hors-bande**
    * Systèmes de messagerie chiffrée
    * Réseaux alternatifs de secours
    * Systèmes de vidéoconférence sécurisés
    * Moyens de communication physiques de secours
  *   **Points de contact clairement définis**
    * Porte-parole officiel désigné
    * Coordinateurs par département
    * Contacts techniques principaux
    * Responsables décisionnaires
    * Représentants légaux
    * Contacts d'urgence 24/7
  *   **Communication régulière avec les parties prenantes**
    * Rapports de situation périodiques
    * Mises à jour sur l'avancement
    * Points d'information programmés
    * Documentation des échanges
    * Suivi des décisions prises
  *   **Coordination avec les relations publiques pour les communications externes**
    * Stratégie médiatique définie
    * Messages clés validés
    * Processus d'approbation des communiqués
    * Gestion des réseaux sociaux
    * Réponses aux demandes médias
    * Surveillance de la couverture médiatique
  *   **Notification aux autorités réglementaires si nécessaire**
    * Identification des obligations légales
    * Délais de notification à respecter
    * Formats de déclaration requis
    * Documentation des communications
    * Suivi des réponses reçues
    * Mise à jour des autorités concernées

## 7. Conformité Réglementaire

De nombreuses réglementations imposent des **obligations en matière de réponse aux incidents** :

*   **Exigences typiques** :
  *   **Notification aux autorités dans des délais spécifiques**
    * RGPD : 72 heures maximum après la découverte
    * Notification à la CNIL en France
    * Format de déclaration standardisé
    * Description détaillée de l'incident
    * Mesures de protection mises en place
    * Évaluation des risques potentiels
  *   **Information des personnes concernées par une violation de données**
    * Communication claire et transparente
    * Description des données compromises
    * Risques potentiels pour les personnes
    * Mesures de protection recommandées
    * Contact pour plus d'informations
    * Délais raisonnables d'information
  *   **Documentation des mesures de réponse**
    * Chronologie détaillée des actions
    * Personnes impliquées dans la réponse
    * Décisions prises et justifications
    * Mesures correctives appliquées
    * Résultats des actions entreprises
    * Leçons apprises
  *   **Conservation des preuves**
    * Durée légale de conservation
    * Stockage sécurisé des données
    * Accès restreint et contrôlé
    * Copies de sauvegarde sécurisées
    * Traçabilité des accès
    * Protection contre l'altération
  *   **Analyse d'impact des violations de données**
    * Évaluation de la gravité
    * Identification des données touchées
    * Impact sur les droits des personnes
    * Conséquences potentielles
    * Probabilité de récurrence
    * Recommandations d'amélioration

## 8. Simulation et Exercices

Les **exercices de simulation** sont essentiels pour tester et améliorer la capacité de réponse aux incidents.

*   **Types d'exercices** :
  *   **Exercices sur table** : Discussions théoriques sur des scénarios
  *   **Exercices fonctionnels** : Tests de composants spécifiques du plan
  *   **Exercices à grande échelle** : Simulations complètes impliquant toute l'organisation
  *   **Red Team/Blue Team** : Exercices où une équipe simule des attaques tandis que l'autre défend

## 9. Automatisation de la Réponse

L'**automatisation** peut améliorer significativement l'efficacité de la réponse aux incidents.

*   **Avantages** :
  *   Réduction du temps de réponse
  *   Standardisation des processus
  *   Diminution des erreurs humaines
  *   Traitement d'un plus grand volume d'incidents

*   **Exemples d'automatisation** :
  *   Isolement automatique des endpoints compromis
  *   Blocage automatique des adresses IP malveillantes
  *   Corrélation automatique des alertes
  *   Génération de rapports d'incidents

## 10. Métriques et Amélioration Continue

Les **métriques** permettent d'évaluer l'efficacité du processus de réponse aux incidents et de l'améliorer continuellement.

*   **Indicateurs clés** :
  *   **Temps moyen de détection (MTTD)**
    * Formule : MTTD = Σ(Temps de détection - Temps de début de l'incident) / Nombre total d'incidents
    * Unité : Heures ou jours
    * Exemple : Si 3 incidents ont été détectés en 2h, 4h et 6h, MTTD = (2+4+6)/3 = 4h
    * Objectif : Réduire ce temps au minimum
    * Facteurs d'influence : Outils de détection, formation du personnel
  *   **Temps moyen de réponse (MTTR)**
    * Formule : MTTR = Σ(Temps de résolution - Temps de détection) / Nombre total d'incidents
    * Unité : Heures ou jours
    * Exemple : Si 3 incidents ont été résolus en 3h, 5h et 7h, MTTR = (3+5+7)/3 = 5h
    * Objectif : Minimiser le temps de réponse
    * Facteurs d'influence : Procédures, ressources disponibles
  *   **Pourcentage d'incidents résolus**
    * Formule : (Nombre d'incidents résolus / Nombre total d'incidents) × 100
    * Unité : Pourcentage
    * Exemple : 45 incidents résolus sur 50 = (45/50) × 100 = 90%
    * Objectif : Maximiser le taux de résolution
    * Benchmark : Viser >95%
  *   **Coût moyen par incident**
    * Formule : Σ(Coûts directs + Coûts indirects) / Nombre total d'incidents
    * Composants : Main d'œuvre, outils, pertes d'activité, impact réputation
    * Exemple : Si 3 incidents ont coûté 1000€, 2000€ et 3000€, moyenne = 2000€
    * Objectif : Réduire les coûts par incident
    * Facteurs : Gravité, durée, ressources nécessaires
  *   **Taux de récurrence des incidents**
    * Formule : (Nombre d'incidents récurrents / Nombre total d'incidents) × 100
    * Unité : Pourcentage
    * Exemple : 5 incidents récurrents sur 50 = (5/50) × 100 = 10%
    * Objectif : Minimiser les récurrences
    * Actions : Analyse des causes profondes
  *   **Efficacité des contrôles de sécurité**
    * Formule : (Incidents bloqués / Total des tentatives d'incidents) × 100
    * Mesures complémentaires : Faux positifs, faux négatifs
    * Exemple : 90 incidents bloqués sur 100 = 90% d'efficacité
    * Objectif : Maximiser l'efficacité des contrôles
    * Évaluation : Tests réguliers et audits