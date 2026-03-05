# Méthodologie d'une attaque ciblée (De la reconnaissance à l'exploitation)

Ce chapitre détaille les étapes clés qu'un attaquant suit généralement lors d'une attaque ciblée, en mettant l'accent sur la méthodologie, les outils et les techniques employés.  Comprendre ces étapes est crucial pour mettre en place des défenses efficaces.

Attaque à la mode:

*   **Les plateformes mobiles (Android, iOS) :** Cible prioritaire des attaques en raison de leur large utilisation et des vulnérabilités potentielles.
*   **Utilisation de smartphones infectés pour des attaques distribuées :** Les smartphones peuvent être enrôlés dans des botnets pour lancer des attaques DDoS.
*   **Intérêt croissant pour les solutions bancaires et de paiement mobile :** Les applications bancaires et de paiement sont des cibles lucratives pour les attaquants.
*   **Utilisation de la puissance de calcul des appareils (pour miner du Bitcoin) :** Le "cryptojacking" consiste à utiliser la puissance de calcul des appareils infectés pour miner des cryptomonnaies.
*   **Les objets connectés (IoT) comme vecteur d'attaque :** Les appareils IoT sont souvent mal sécurisés et peuvent être utilisés comme points d'entrée dans un réseau.
*   **Intérêt pour les données biométriques et de santé :** Les données biométriques et de santé sont très sensibles et peuvent être utilisées pour l'usurpation d'identité ou le chantage.

## Méthodologie d'une attaque ciblée

### Collecte d'informations (Reconnaissance)

La phase de reconnaissance est cruciale et consiste à recueillir le maximum d'informations sur la cible avant de lancer l'attaque.

1.  **Connaitre sa cible :** Déterminer le type d'organisation, son secteur d'activité, sa taille, sa structure, ses technologies, ses employés clés, ses partenaires, etc.

2.  **Google est notre ami (OSINT - Open Source Intelligence) :** Utiliser les moteurs de recherche (Google, DuckDuckGo, etc.) pour trouver des informations publiquement disponibles sur la cible :
  *   Sites web, blogs, forums.
  *   Profils sur les réseaux sociaux (LinkedIn, Twitter, Facebook, etc.).
  *   Articles de presse, rapports, documents publics.
  *   Informations sur les employés, les technologies utilisées, les adresses IP, les noms de domaine.

3.  **Les humains sont bavards :** L'ingénierie sociale est un vecteur d'attaque puissant. Exploiter la confiance ou la naïveté des employés pour obtenir des informations sensibles (mots de passe, identifiants, informations sur les systèmes). (cf Section 14 du `paste.txt` sur l'ingenierie sociale)

4.  **Quelques commandes utiles (reconnaissance réseau) :**
  *   `ping` : Vérifier si une machine est accessible sur le réseau.
  *   `traceroute` (ou `tracert` sous Windows) : Afficher le chemin suivi par les paquets pour atteindre une cible.
  *   `nslookup` / `dig` : Interroger les serveurs DNS pour obtenir des informations sur les noms de domaine et les adresses IP.
  *   `whois` : Obtenir des informations sur le propriétaire d'un nom de domaine ou d'une adresse IP.

5.  **Prise d'empreintes (fingerprinting) :** Identifier le système d'exploitation, les applications et les services qui fonctionnent sur les machines de la cible :
  *   Analyse des en-têtes HTTP.
  *   Utilisation d'outils comme Nmap ([https://nmap.org/](https://nmap.org/)) pour scanner les ports ouverts et identifier les services en cours d'exécution.

6.  **Interroger les services accessibles :** Une fois les services identifiés, tenter d'obtenir des informations plus précises sur leurs versions, leurs configurations et leurs vulnérabilités potentielles.

### Repérage des failles (Analyse des vulnérabilités)

Une fois la phase de reconnaissance terminée, l'attaquant se concentre sur l'identification des vulnérabilités qui peuvent être exploitées.

1.  **Consulter les failles recensées :**
*   Utiliser des bases de données de vulnérabilités comme CVE (Common Vulnerabilities and Exposures) ([https://cve.mitre.org/](https://cve.mitre.org/)) ou NVD (National Vulnerability Database) ([https://nvd.nist.gov/](https://nvd.nist.gov/)) pour rechercher les vulnérabilités connues affectant les logiciels et les systèmes utilisés par la cible.

2.  **Éliminer les failles non fondées :** Valider la présence et l'exploitabilité des vulnérabilités identifiées :
*   Tests manuels.
*   Utilisation d'outils d'analyse de vulnérabilités (ex: Nessus, OpenVAS, metasploit).

### Intrusion dans le système (Exploitation)

Cette phase consiste à exploiter les vulnérabilités identifiées pour obtenir un accès non autorisé au système cible.

1.  **Ne pas laisser de traces :** Tenter de minimiser les traces de l'intrusion pour éviter d'être détecté (utilisation de techniques d'offuscation, suppression de logs, etc.).
2.  **Extension de privilèges (Privilege Escalation) :** Une fois un accès initial obtenu (même avec des privilèges limités), tenter d'élever ses privilèges pour obtenir un contrôle plus important sur le système (ex : exploitation de vulnérabilités du système d'exploitation, vol de mots de passe administrateur).
3.  **Collecte d'informations (depuis l'intérieur) :** Une fois à l'intérieur du système, recueillir des informations supplémentaires sur l'architecture, les configurations, les utilisateurs, les données sensibles, etc.

### Assurer son accès (Persistance)

Pour maintenir un accès durable au système cible, l'attaquant met en place des mécanismes de persistance.

1.  **Exploiter les relations des machines (Lateral Movement) :** Utiliser les informations d'identification volées ou les vulnérabilités découvertes sur d'autres machines du réseau pour se déplacer latéralement et accéder à des systèmes plus intéressants.
2.  **Écouter le trafic (Sniffing) :** Intercepter le trafic réseau pour capturer des informations sensibles (mots de passe, identifiants, données confidentielles).
3.  **Faciliter son retour (Backdoors) :** Installer des portes dérobées (backdoors) pour pouvoir accéder au système ultérieurement, même si les vulnérabilités initiales sont corrigées.

### Exploitation (Objectifs)

L'étape finale consiste à atteindre les objectifs de l'attaque (vol de données, sabotage, espionnage, etc.) en utilisant l'accès et les informations obtenus précédemment.

**Voir démonstration nmap**



