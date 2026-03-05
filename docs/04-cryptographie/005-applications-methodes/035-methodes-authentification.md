# Les méthodes d'authentification

## Introduction

L'authentification est un processus crucial pour sécuriser l'accès aux systèmes et aux réseaux. Voici trois méthodes d'authentification couramment utilisées : PAP, CHAP et Kerberos.

## PAP (Password Authentication Protocol)

PAP est un protocole d'authentification simple où le nom d'utilisateur et le mot de passe sont transmis **en clair**.

### Caractéristiques

- **Simplicité** : Facile à mettre en œuvre
- **Insécurité** : Les informations d'identification sont envoyées sans chiffrement
- **Utilisation** : Déconseillée pour les environnements non sécurisés

### Fonctionnement 

Le fonctionnement de PAP peut être comparé à une simple vérification d'identité à l'entrée d'un bâtiment. L'utilisateur (le client) se présente au gardien (le serveur) et lui donne directement son nom et son mot de passe, comme si vous montriez une carte d'identité en clair. Le gardien compare ces informations à une liste qu'il possède (la base de données des utilisateurs) pour vérifier leur validité. Si elles correspondent, l'accès est accordé. Cependant, comme les informations sont transmises sans protection (en clair), n'importe qui observant la conversation pourrait facilement les intercepter et les utiliser, ce qui rend ce processus peu sécurisé.

Exemple d'utilisation de PAP

*  Le protocole PAP (Password Authentication Protocol) est utilisé dans plusieurs scénarios spécifiques, bien qu'il soit considéré comme peu sécurisé. Voici quelques exemples :
  *  Legacy Systems : PAP est souvent utilisé dans les systèmes anciens où les exigences de sécurité sont minimales ou où la compatibilité avec des équipements obsolètes est nécessaire15.
  *  Liaisons PPP (Point-to-Point Protocol) : PAP est couramment employé pour l'authentification, notamment pour établir des sessions réseau simples entre deux points, comme dans les connexions modem ou certaines configurations VPN basiques23.
  *  Environnements contrôlés : Dans des réseaux fermés ou sécurisés où le risque d'interception est faible, PAP peut être utilisé pour simplifier l'authentification.
  *  Fallback Authentication : PAP peut servir de méthode de secours lorsque des protocoles plus sécurisés, comme CHAP ou EAP, échouent ou ne sont pas pris en charge.

Ces cas d'utilisation montrent que PAP est principalement adapté à des environnements où la sécurité n'est pas une priorité absolue et où la simplicité ou la compatibilité avec des systèmes anciens est recherchée.

## CHAP (Challenge-Handshake Authentication Protocol)

CHAP est un protocole d'authentification plus sécurisé que PAP, utilisant un mécanisme de **défi-réponse**.

### Fonctionnement

1. **Envoi du défi** : Le serveur envoie un défi au client.
2. **Réponse du client** : Le client répond avec un hash du défi combiné au mot de passe.
3. **Vérification** : Le serveur vérifie la réponse.

Le fonctionnement de CHAP peut être comparé à un jeu de devinettes sécurisé entre un gardien (le serveur) et un visiteur (le client) à l'entrée d'un lieu secret. Voici comment cela se déroule : d'abord, le gardien pose une question énigmatique unique (le défi) au visiteur. Ensuite, le visiteur utilise cette énigme et un code secret qu'il partage avec le gardien pour créer une réponse spéciale (le hash). Enfin, le gardien, qui connaît aussi le code secret, vérifie si la réponse du visiteur est correcte. Si c'est le cas, le visiteur est autorisé à entrer. Ce processus est plus sûr qu'un simple mot de passe car l'énigme change à chaque fois, rendant impossible pour quelqu'un qui écouterait la conversation de réutiliser les réponses précédentes pour entrer

### Avantages

- **Sécurité accrue** : Le mot de passe n'est jamais transmis en clair.
- **Protection contre les attaques par rejeu** : Le défi change à chaque authentification.

### Exemple d'utilisation de CHAP

Le protocole CHAP (Challenge Handshake Authentication Protocol) est largement utilisé dans divers environnements de mise en réseau pour une authentification sécurisée. Voici quelques exemples :

* **Accès à distance sécurisé** : CHAP est couramment employé pour authentifier les utilisateurs lors de connexions à distance, offrant une meilleure sécurité que PAP.
* **Réseaux privés virtuels (VPN)** : CHAP est fréquemment utilisé dans les configurations VPN pour établir une connexion sécurisée entre le client et le serveur.
* **Connexions de fournisseurs de services Internet (ISP)** : De nombreux ISP utilisent CHAP pour authentifier leurs clients lors de l'établissement de connexions Internet.
* **Authentification iSCSI** : CHAP est utilisé dans le protocole iSCSI pour permettre l'authentification mutuelle entre l'initiateur et la cible iSCSI.
* **Environnements de stockage** : CHAP peut être utilisé pour vérifier si une demande de connexion au système de stockage provient d'un nœud de calcul valide, notamment dans les connexions iSCSI.
* **Réseaux d'entreprise** : CHAP est souvent préféré dans les réseaux d'entreprise où une authentification plus robuste est nécessaire pour protéger les ressources sensibles.

Ces cas d'utilisation démontrent que CHAP est adapté aux environnements nécessitant un niveau de sécurité plus élevé que PAP, en particulier lorsqu'une authentification forte et une protection contre les attaques par rejeu sont requises.

## Kerberos

### Définition

Kerberos est un protocole d'authentification réseau conçu pour fournir une **authentification forte** pour les applications client/serveur.

### Caractéristiques principales

- **Authentification mutuelle** : Le client et le serveur s'authentifient l'un à l'autre.
- **Utilisation de tickets** : Des tickets chiffrés sont utilisés pour prouver l'identité.
- **Serveur central** : Un serveur d'authentification central gère les identités.

### Fonctionnement

1. **Authentification initiale** : L'utilisateur s'authentifie auprès du serveur Kerberos.
2. **Ticket Granting Ticket (TGT)** : Le serveur Kerberos fournit un TGT.
3. **Tickets de service** : Le TGT est utilisé pour obtenir des tickets de service spécifiques.
4. **Accès aux ressources** : Les tickets de service permettent l'accès aux ressources du réseau.

Le fonctionnement de Kerberos peut être comparé à un système de billetterie pour un parc d'attractions. Tout commence à l'entrée : l'utilisateur (visiteur) s'identifie auprès du guichet principal (serveur Kerberos) et prouve qu'il est autorisé à entrer. En retour, il reçoit un Ticket Granting Ticket (TGT), qui agit comme un bracelet spécial permettant d'accéder aux différentes attractions. Lorsqu'il veut profiter d'une attraction particulière (une ressource réseau), il utilise son TGT pour obtenir un ticket spécifique auprès du guichet interne (serveur de tickets). Ce ticket spécifique est ensuite présenté à l'attraction (la ressource), qui vérifie sa validité avant de lui accorder l'accès. Ainsi, Kerberos garantit que chaque interaction est sécurisée et que seules les personnes autorisées peuvent accéder aux services.

### Avantages

- **Haute sécurité** : Utilisation de cryptographie forte.
- **Single Sign-On (SSO)** : L'utilisateur ne s'authentifie qu'une seule fois.
- **Évolutivité** : Adapté aux grands réseaux d'entreprise.

### Exemple d'utilisation de Kerberos

Le protocole Kerberos est largement utilisé dans divers environnements pour garantir une authentification sécurisée et fiable. Voici quelques exemples de cas d'utilisation :

* **Réseaux d'entreprise** : Kerberos est couramment utilisé pour authentifier les utilisateurs et les services dans des réseaux distribués, en particulier dans des environnements Windows via Active Directory.
* **Single Sign-On (SSO)** : Kerberos permet aux utilisateurs de s'authentifier une seule fois pour accéder à plusieurs ressources sans avoir à entrer leurs identifiants à chaque fois.
* **Environnements distribués** : Dans des systèmes complexes où plusieurs serveurs et services interagissent, Kerberos garantit une authentification mutuelle sécurisée entre les clients et les serveurs.
* **Applications client-serveur** : Les applications qui nécessitent une authentification mutuelle (client et serveur) utilisent souvent Kerberos pour sécuriser leurs communications.
* **Systèmes Unix/Linux** : Kerberos est intégré dans de nombreux systèmes Unix/Linux pour gérer l'authentification des utilisateurs et des services.
* **Accès à distance sécurisé** : Les organisations utilisent Kerberos pour sécuriser l'accès aux ressources sensibles depuis des appareils approuvés, même sur des réseaux non sécurisés.

Ces cas d'utilisation montrent que Kerberos est adapté aux environnements nécessitant une sécurité élevée, une authentification mutuelle et une gestion centralisée des identités.