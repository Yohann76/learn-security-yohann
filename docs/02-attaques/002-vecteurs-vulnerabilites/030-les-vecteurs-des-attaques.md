# Les vecteurs d'attaques

* Les vecteurs d'attaque sont les méthodes utilisées par les attaquants pour pénétrer dans les systèmes.

  * Ingénierie sociale
    * Définition : Manipuler des individus pour obtenir des informations ou un accès non autorisé.
      * Concept de base : Exploiter la confiance et la naïveté des personnes.
      * Ingénierie sociale inverse : Se faire contacter par la victime en se faisant passer pour une ressource.
      * Baiting : Utiliser un appât (clé USB infectée, etc.) pour inciter la victime à agir.
      * Phishing : Envoyer des e-mails frauduleux pour voler des informations personnelles.
      * Pretexting : Créer un scénario pour obtenir des informations confidentielles.

  * Logiciels malicieux (malware)
    * Définition : Logiciels conçus pour causer des dommages ou obtenir un accès non autorisé.
      * Virus : Se propage en infectant des fichiers.
      * Vers : Se propage automatiquement à travers les réseaux.
      * Rootkit : Masque la présence d'autres logiciels malveillants.
      * Troyen : Se déguise en logiciel légitime pour tromper l'utilisateur.
      * Spyware : Collecte des informations sur l'utilisateur sans son consentement.
      * Ransomware : Chiffre les fichiers de la victime et exige une rançon pour les déchiffrer.
      * Keylogger : Enregistre les frappes au clavier pour voler des mots de passe et autres informations.
      * Sniffer réseau : Intercepte le trafic réseau pour voler des informations.
      * Dialer : Utilise la connexion téléphonique pour composer des numéros surtaxés.

### Classification des attaques selon la couche ciblée

**Modele OSI**

![](../../images/modele-osi.png)


1.  **Intrusions de niveau 1 : Attaques au niveau de la couche Physique (Physical Layer)**
    *   **Cible :** Câbles, connecteurs, équipements réseau physiques (hubs, répéteurs).
    *   **Description :** Ces attaques ciblent directement l'infrastructure physique du réseau, en exploitant des vulnérabilités liées à la sécurité des équipements ou à l'accès physique aux câbles et aux connecteurs.
    *   **Exemples :**
      *   **Écoute physique (Wiretapping) :** L'attaquant se connecte physiquement à un câble réseau pour intercepter les signaux électriques et écouter le trafic réseau.
      *   **Sabotage physique :** L'attaquant endommage ou détruit des câbles, des connecteurs ou des équipements réseau pour provoquer une interruption de service.
      *   **Vol d'équipement :** L'attaquant vole des équipements réseau (routeurs, commutateurs, serveurs) pour accéder aux données ou perturber le fonctionnement du réseau.
      *   **Interférence électromagnétique (EMI) :** L'attaquant utilise des dispositifs pour générer des interférences électromagnétiques et perturber la transmission des données sur les câbles réseau.
      *   **Accès non autorisé aux locaux :** L'attaquant pénètre physiquement dans les locaux où se trouvent les équipements réseau pour les manipuler, les voler ou y installer des dispositifs d'écoute.
    *   **Conséquences :** Interruption de service, perte de données, compromission d'informations sensibles, accès non autorisé au réseau.

2.  **Intrusions de niveau 2 : Attaques au niveau de la couche Liaison de données (Data Link Layer)**
    *   **Cible :** Commutateurs d'accès (switches) et points d'accès sans fil (Wi-Fi).
    *   **Description :** Ces attaques exploitent les vulnérabilités des protocoles de communication utilisés au niveau de la couche 2, comme Ethernet ou Wi-Fi.
    *   **Exemples :**
      *   **Attaques ARP Spoofing :** L'attaquant associe sa propre adresse MAC à l'adresse IP d'une autre machine sur le réseau, lui permettant d'intercepter le trafic destiné à cette machine.
      *   **Attaques MAC Flooding :** L'attaquant inonde le commutateur avec de nombreuses adresses MAC différentes, surchargeant sa table d'adresses MAC et le forçant à diffuser le trafic à toutes les machines du réseau (comme un hub).
      *   **Attaques contre le protocole Spanning Tree (STP) :** L'attaquant manipule le protocole STP pour se faire élire comme commutateur racine, lui permettant de contrôler le flux du trafic sur le réseau.
      *   **Attaques contre les réseaux Wi-Fi :**
          *   **Attaques par force brute contre les mots de passe Wi-Fi.**
          *   **Création de faux points d'accès (Evil Twin) pour piéger les utilisateurs.**
          *   **Attaques de désauthentification pour forcer les utilisateurs à se reconnecter à un point d'accès contrôlé par l'attaquant.**
    *   **Conséquences :** Interception de trafic, déni de service, compromission de données.

3.  **Intrusions de niveau 3 : Attaques au niveau de la couche Réseau (Network Layer)**
    *   **Cible :** Protocole IP (Internet Protocol) et services réseau associés.
    *   **Description :** Ces attaques exploitent les vulnérabilités du protocole IP et des applications qui l'utilisent pour communiquer sur le réseau.
    *   **Exemples :**
      *   **IP Spoofing :** L'attaquant falsifie l'adresse IP source des paquets qu'il envoie, permettant de masquer son identité ou de lancer des attaques par déni de service.
      *   **Attaques par déni de service (DoS) :** L'attaquant surcharge un serveur ou un réseau avec un grand nombre de requêtes, le rendant indisponible pour les utilisateurs légitimes.
      *   **Scans réseau (Port Scanning) :** L'attaquant explore les ports ouverts d'un système pour identifier les services qui y sont exécutés et les vulnérabilités potentielles.
      *   **Sniffing :** L'attaquant intercepte le trafic réseau pour voler des informations sensibles (mots de passe, données bancaires, etc.).
      *   **Attaques de type Man-in-the-Middle (MitM) :** L'attaquant se positionne entre deux parties qui communiquent et intercepte ou modifie leurs échanges.
      *   **Attaques contre les applications stratégiques :**
          *   **DHCP (Dynamic Host Configuration Protocol) :** L'attaquant peut configurer de faux serveurs DHCP pour distribuer de fausses adresses IP et rediriger le trafic des utilisateurs vers des serveurs malveillants.
          *   **DNS (Domain Name System) :** L'attaquant peut empoisonner le cache DNS pour rediriger les utilisateurs vers de faux sites web.
          *   **SMTP (Simple Mail Transfer Protocol) :** L'attaquant peut utiliser un serveur SMTP compromis pour envoyer du spam ou des e-mails de phishing.
      *   **Attaques contre les applications à risques :**
          *   **HTTP (Hypertext Transfer Protocol) :** L'attaquant peut exploiter les vulnérabilités des applications web (injection SQL, Cross-Site Scripting, etc.) pour voler des données, compromettre des serveurs ou rediriger les utilisateurs vers des sites malveillants.
    *   **Conséquences :** Interception de trafic, déni de service, vol de données, compromission de systèmes.

4.  **Intrusions de niveau 4 : Attaques au niveau de la couche Transport (Transport Layer)**
    *   **Cible :** Protocoles TCP (Transmission Control Protocol) et UDP (User Datagram Protocol).
    *   **Description :** Ces attaques exploitent les vulnérabilités des protocoles de transport utilisés pour établir et maintenir les connexions entre les applications.
    *   **Exemples :**
      *   **Attaques SYN Flood (TCP) :** L'attaquant envoie un grand nombre de requêtes de connexion SYN à un serveur, sans jamais répondre aux confirmations SYN-ACK. Cela sature les ressources du serveur et l'empêche de traiter les requêtes légitimes.
      *   **Attaques UDP Flood :** L'attaquant envoie un grand volume de paquets UDP à un serveur, surchargeant sa bande passante et ses ressources de traitement.
      *   **Attaques de type Port Scanning (TCP/UDP) :** L'attaquant explore les ports ouverts d'un système pour identifier les services qui y sont exécutés et les vulnérabilités potentielles. (Bien que le scan réseau commence au niveau 3, l'identification des services spécifiques se fait souvent en interagissant avec les ports TCP/UDP ouverts).
      *   **Session Hijacking (TCP) :** L'attaquant intercepte une session TCP active entre un client et un serveur, lui permettant de prendre le contrôle de la connexion et d'usurper l'identité du client.
    *   **Conséquences :** Déni de service, interception de données, compromission de sessions.

**Voir démonstration ftp-trame (Espionnage sur le réseau)**


