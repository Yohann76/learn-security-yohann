# Concepts de la cryptographie

La cryptographie est l'étude des techniques de communication sécurisée en présence d'adversaires. 

Elle englobe un ensemble de méthodes pour chiffrer, déchiffrer, authentifier et protéger les informations. 

C'est la science qui permet de transformer des messages ordinaires en codes secrets, compréhensibles uniquement par les personnes autorisées

C'est l'art de cacher des informations.

Imaginez une enveloppe magique qui rend son contenu illisible à tous sauf au destinataire prévu.

La cryptographie est essentielle pour la confidentialité, l'intégrité et l'authenticité des données dans le monde numérique moderne.

## Concepts Fondamentaux

### Chiffrement (Encryption)

Le chiffrement est le processus de transformation des données (appelées texte clair) en une forme illisible (appelée texte chiffré) à l'aide d'un algorithme de chiffrement et d'une clé. L'objectif est de rendre les données inaccessibles à toute personne ne possédant pas la clé de déchiffrement.

*   **Texte Clair (Plaintext) :** Les données originales, lisibles par l'homme.
*   **Texte Chiffré (Ciphertext) :** Les données transformées, illisibles sans la clé de déchiffrement.
*   **Algorithme de Chiffrement :** La méthode mathématique utilisée pour transformer le texte clair en texte chiffré.
*   **Clé de Chiffrement :** Une valeur secrète utilisée avec l'algorithme pour chiffrer les données.

### Déchiffrement (Decryption)

Le déchiffrement est le processus inverse du chiffrement. 
Il consiste à transformer le texte chiffré en texte clair à l'aide d'un algorithme de déchiffrement et d'une clé.

*   **Algorithme de Déchiffrement :** La méthode mathématique utilisée pour transformer le texte chiffré en texte clair.
*   **Clé de Déchiffrement :** Une valeur secrète utilisée avec l'algorithme pour déchiffrer les données.

### Clé (Key)

Une clé est une valeur secrète utilisée par un algorithme de chiffrement ou de déchiffrement. La sécurité de la cryptographie repose sur la confidentialité et la robustesse des clés.

*   **Clé Secrète (Secret Key) :** Utilisée dans le chiffrement symétrique, où la même clé est utilisée pour chiffrer et déchiffrer les données.
*   **Clé Publique (Public Key) :** Utilisée dans le chiffrement asymétrique, où une clé est distribuée publiquement pour chiffrer les données, tandis qu'une clé privée correspondante est utilisée pour les déchiffrer.
*   **Clé Privée (Private Key) :** Utilisée dans le chiffrement asymétrique, elle est gardée secrète par son propriétaire et utilisée pour déchiffrer les données chiffrées avec la clé publique correspondante.

### Algorithme

Un algorithme est une série d'étapes mathématiques utilisées pour chiffrer ou déchiffrer les données. La sécurité de l'algorithme repose sur sa complexité et sa résistance aux attaques cryptanalytiques.

### Hachage

Le hachage est le processus de transformation des données en une empreinte numérique de taille fixe (appelée haché) à l'aide d'une fonction de hachage. Le hachage est utilisé pour vérifier l'intégrité des données, stocker les mots de passe de manière sécurisée, et créer des signatures numériques.

*   **Fonction de Hachage :** Un algorithme mathématique qui prend des données en entrée et produit un haché de taille fixe.
*   **Haché (Hash) :** L'empreinte numérique des données, utilisée pour vérifier l'intégrité.

### Signature numérique (Digital Signature)

Une signature numérique est une technique cryptographique utilisée pour authentifier l'origine d'un message ou d'un document, et pour vérifier son intégrité. 
Elle est créée à l'aide de la clé privée de l'expéditeur et peut être vérifiée par toute personne possédant la clé publique correspondante.

Une signature numérique est comme un sceau de cire personnalisé et inimitable sur une lettre ancienne 
elle prouve l'identité de l'expéditeur et garantit que le contenu n'a pas été altéré depuis son cachetage, tout en permettant à quiconque de vérifier son authenticité.

### Certificat numérique (Digital Certificate)

Un certificat numérique est un document électronique qui atteste de l'identité d'une personne, d'une organisation ou d'un serveur. Il est émis par une autorité de certification (CA) et contient la clé publique de l'entité certifiée, ainsi que des informations sur son identité.

*  Imaginez que vous souhaitez accéder à votre compte bancaire en ligne. Lorsque vous vous connectez au site web de votre banque, votre navigateur vérifie automatiquement le certificat numérique du site. Ce certificat contient :
  *  L'identité de la banque (nom, adresse, etc.)
  *  La clé publique du site web de la banque
  *  La signature de l'autorité de certification qui a émis le certificat
  *  La période de validité du certificat
  *  Votre navigateur utilise ce certificat pour :
  *  Vérifier que vous êtes bien sur le vrai site de votre banque
  *  Établir une connexion sécurisée et chiffrée avec le site

Ce processus se déroule en arrière-plan, assurant une certaine sécurité sans que vous ayez à intervenir.

## Propriétés éssentielles des algorithmes cryptographiques

### Confidentialité

Les algorithmes de chiffrement doivent garantir que les données chiffrées ne peuvent être lues que par les personnes autorisées, c'est-à-dire celles qui possèdent la clé de déchiffrement.

### Intégrité

Les algorithmes de hachage et de signature numérique doivent garantir que les données n'ont pas été modifiées ou altérées pendant leur transmission ou leur stockage.

### Authentification

Les algorithmes de signature numérique doivent permettre de vérifier l'identité de l'expéditeur d'un message ou d'un document, et de s'assurer qu'il est bien celui qu'il prétend être.

## Attaques cryptanalytiques

La cryptanalyse est l'étude des méthodes pour casser les systèmes cryptographiques, c'est-à-dire pour déchiffrer les données sans connaître la clé, pour falsifier les signatures numériques, ou pour trouver des collisions de hachage.

*   **Attaque par Force Brute :** Essayer toutes les clés possibles jusqu'à trouver la bonne.
*   **Attaque par Dictionnaire :** Essayer les mots de passe les plus courants.
*   **Attaque par Analyse de Fréquences :** Analyser la fréquence des caractères ou des motifs dans le texte chiffré pour déduire des informations sur le texte clair.
*   **Attaque de l'Homme du Milieu :** Intercepter les communications entre deux parties et les modifier ou les rediriger.
*   **Attaque par Canal Latéral :** Exploiter les informations divulguées par l'implémentation physique de l'algorithme, telles que la consommation d'énergie, le temps d'exécution ou les émissions électromagnétiques.

## Importance de la cryptographie

La cryptographie est essentielle pour sécuriser les communications, les transactions et les données dans le monde numérique. Elle est utilisée dans de nombreux domaines, tels que :

*   **Commerce Électronique :** Sécurisation des transactions en ligne et protection des informations de carte de crédit.
  *  Lors d'un paiement en ligne, une étape supplémentaire de vérification est ajoutée (par exemple, un code envoyé par SMS ou une validation via une application bancaire). 
     Cela garantit que  seul le titulaire légitime de la carte peut finaliser la transaction
  *  Les informations sensibles, comme les numéros de carte, sont stockées dans des coffres numériques cryptés ou ne sont pas conservées du tout sur les serveurs des marchands
*   **Communications Sécurisées :** Chiffrement des emails, des messages instantanés et des appels téléphoniques.
*   **Sécurité des Réseaux :** Protection des réseaux informatiques contre les intrusions et les attaques.
  *  WPA3 pour Wi-Fi sécurisé
*   **Authentification :** Vérification de l'identité des utilisateurs et des systèmes.
  *  Authentification par certificat numérique : Les sites web sécurisés utilisent des certificats SSL/TLS pour prouver leur identité aux navigateurs.
  *  Authentification multifactorielle (MFA) : En plus d'un mot de passe, l'utilisateur doit fournir un second facteur d'authentification, comme un code temporaire généré par une application d'authentification. Ce code est cryptographiquement lié à l'appareil de l'utilisateur. 
  *  Authentification biométrique : Les smartphones utilisent des techniques cryptographiques pour sécuriser les données biométriques (empreintes digitales, reconnaissance faciale) stockées localement. Lors de l'authentification, seul le résultat de la vérification est transmis, pas les données biométriques elles-mêmes
  *  Single Sign-On (SSO) avec OAuth : Lorsqu'un utilisateur choisit de "Se connecter avec Google" sur un site tiers, OAuth utilise des jetons cryptographiques pour authentifier l'utilisateur sans partager ses identifiants réels
*   **Protection des Données :** Chiffrement des données sensibles stockées sur les ordinateurs, les serveurs et les appareils mobiles.
  *  BitLocker (Windows) : Cet outil chiffre automatiquement les données sur les disques durs pour empêcher leur accès en cas de perte ou de vol d'un ordinateur portable
  *  FileVault (macOS) : Apple propose FileVault pour chiffrer les disques durs des Mac, protégeant ainsi toutes les données stockées localement.
  *  Chiffrement côté serveur : Les services cloud comme Google Drive ou Dropbox chiffrent les fichiers après leur transfert vers leurs serveurs et les déchiffrent avant leur récupération par l'utilisateur
