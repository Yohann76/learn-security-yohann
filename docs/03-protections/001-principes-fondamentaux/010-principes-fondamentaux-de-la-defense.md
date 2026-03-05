# Principe fondamentaux de la défense

Recommandation de L'ANNSI en matiére de bonne pratique : [Les Dix règles d'or préventives de l'ANNSI](https://cyber.gouv.fr/dix-regles-dor-preventives)

## Les piliers d'une défense solide : Votre plan de bataille

*   La défense ne se limite pas à l'installation de quelques outils. Elle repose sur une approche globale et proactive, articulée autour de plusieurs piliers :
  *   **Évaluation des risques :** Identifier les actifs les plus critiques de votre organisation et les menaces qui pèsent sur eux (cf. Section 6 du `paste.txt`).
  *   **Politiques de sécurité :** Définir des règles claires et précises pour encadrer l'utilisation des systèmes d'information et protéger les données sensibles.
  *   **Mesures techniques :** Mettre en place des solutions de sécurité adaptées à vos besoins (pare-feu, antivirus, systèmes de détection d'intrusion, chiffrement, etc.).
  *   **Formation et sensibilisation des utilisateurs :** Former vos employés aux bonnes pratiques en matière de sécurité et les sensibiliser aux risques (cf. Section 3.3 du `paste.txt`).
  *   **Gestion des incidents :** Mettre en place un plan de gestion des incidents pour réagir rapidement et efficacement en cas d'attaque.

## **Le coût de la défense :** Un investissement indispensable
*   La mise en place d'une défense solide représente un investissement, mais le coût de l'inaction est bien plus élevé.
  *   **Le budget sécurité :** Allouez un budget suffisant à la sécurité informatique, en tenant compte des risques et des enjeux.
  *   **Le retour sur investissement (ROI) :** Considérez la sécurité comme un investissement qui vous permet de protéger vos actifs, de préserver votre réputation et d'éviter des pertes financières importantes.
  *   **L'assurance cyber :** Souscrivez une assurance cyber pour vous protéger contre les conséquences financières d'une violation de données.

## Les grands principes d'une bonne défense.

*  **0. L'importance d'une protection globale**
  *  Concept: Il est **crucial** d'avoir un **ensemble de bonnes protections** en place, car les attaquants **ciblent toujours le point faible** d'un système. **Comme dans un château, on n'attaque pas les murailles, mais les points les plus vulnérables.**
  *  Analogie: **"La chaîne se casse toujours sur le maillon le plus faible."**
  *  Implications:
    *   **Ne négligez aucun aspect de la sécurité**, même ceux qui semblent mineurs.
    *   **Évaluez régulièrement la robustesse** de chaque composant de votre système.
    *   **Renforcez les points faibles** identifiés.
    *   Mettez en place des **contrôles compensatoires** si certains points faibles ne peuvent être corrigés immédiatement.
  *  Bénéfices: Réduit **significativement la surface d'attaque** et **augmente la difficulté** pour un attaquant de compromettre le système.
*  **1. La défense en profondeur (Defense in Depth)**
  *  Concept: Mettre en place **plusieurs couches de sécurité**, de sorte que si une couche est compromise, les autres continuent de protéger les actifs.
  *  Exemples:
    *   Sécurité **physique** (contrôle d'accès aux locaux)
    *   Sécurité **périmétrique** (pare-feu, systèmes de détection d'intrusion)
    *   Sécurité **réseau** (segmentation du réseau, VLAN)
    *   Sécurité des **hôtes** (antivirus, durcissement des systèmes)
    *   Sécurité des **applications** (développement sécurisé, tests de sécurité)
    *   Sécurité des **données** (chiffrement, gestion des droits d'accès)
  *  Bénéfices: Augmente **considérablement la difficulté** pour un attaquant de compromettre le système.
*  **2. Le principe de moindre privilège (Principle of Least Privilege)**
  *  Concept: Accorder aux **utilisateurs et aux processus** uniquement les **droits d'accès minimum** nécessaires pour effectuer leurs tâches.
  *  Exemples:
    *   Utiliser des comptes d'**utilisateurs standard** au lieu de comptes administrateur pour les tâches quotidiennes.
    *   Restreindre l'accès aux **données sensibles** aux seules personnes qui en ont besoin.
    *   Utiliser des **rôles et des groupes** pour gérer les permissions.
  *  Bénéfices: Limite l'impact d'une compromission de compte ou d'une erreur humaine.
*  **3. La segmentation du réseau**
  *  Concept: Diviser le réseau en **plusieurs zones isolées** les unes des autres, en fonction de leur **niveau de sécurité et de leur criticité**.
  *  Exemples:
    *   Séparer le réseau des **serveurs critiques** du réseau des utilisateurs.
    *   Créer un réseau **DMZ (Demilitarized Zone)** pour héberger les serveurs accessibles depuis l'extérieur.
    *   Utiliser des **VLAN (Virtual LAN)** pour isoler les différents segments du réseau.
  *  Bénéfices: Limite la propagation d'une attaque en cas de compromission d'une zone.
*  **4. La surveillance et la détection**
  *  Concept: Mettre en place des outils et des processus pour **surveiller les systèmes et les réseaux**, **détecter les activités suspectes** et **réagir rapidement en cas d'incident**.
  *  Exemples:
    *   Systèmes de **détection d'intrusion (IDS)** et systèmes de **prévention d'intrusion (IPS)**
    *   **SIEM (Security Information and Event Management)**
    *   Analyse des **journaux d'événements (logs)**
    *   Surveillance du **trafic réseau**
  *  Bénéfices: Permet de **détecter les attaques en temps réel** et de **réagir rapidement** pour limiter les dommages.
*  **5. La gestion des correctifs (Patch Management)**
  *  Concept: Appliquer **régulièrement les correctifs de sécurité** publiés par les fournisseurs de logiciels pour corriger les vulnérabilités connues.
  *  Processus:
    *   **Identifier** les correctifs disponibles.
    *   **Tester** les correctifs dans un environnement de test avant de les déployer en production.
    *   **Déployer** les correctifs de manière centralisée et automatisée.
  *  Bénéfices: Réduit **considérablement la surface d'attaque** en corrigeant les vulnérabilités connues.
*  **6. La sauvegarde et la restauration**
  *  Concept: Effectuer des **sauvegardes régulières** des données et des systèmes, et mettre en place un **plan de restauration** pour pouvoir récupérer rapidement les données en cas d'incident.
  *  Points clés:
    *   **Automatiser** les sauvegardes.
    *   **Stocker** les sauvegardes dans un endroit sûr et distinct du site de production.
    *   **Tester régulièrement** la procédure de restauration.
  *  Bénéfices: Permet de récupérer les données et les systèmes en cas de perte de données, de ransomware ou de catastrophe naturelle.


