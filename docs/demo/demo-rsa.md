# Démonstration RSA avec OpenSSL

Cette démonstration vous guide à travers les étapes de chiffrement et de déchiffrement d'un message en utilisant l'algorithme RSA et l'outil `openssl` sur Linux.

## Prérequis

* Une machine virtuelle Linux (Ubuntu, Debian, etc.)
* Un terminal
* `openssl` (installez-le si nécessaire)

## Étapes

1.  **Installation d'OpenSSL (si nécessaire)**

    * Ouvrez un terminal et exécutez la commande suivante :

        ```bash
        sudo apt install openssl
        ```

2.  **Génération de la clé privée**

    * Générez une clé privée RSA de 2048 bits :

        ```bash
        openssl genrsa -out private.pem 2048
        ```

    * Vérifiez que la clé privée a été créée :

        ```bash
        ls
        ```

3.  **Extraction de la clé publique**

    * Extrayez la clé publique de la clé privée :

        ```bash
        openssl rsa -in private.pem -out public.pem -outform PEM -pubout
        ```

4.  **Création du message secret**

    * Créez un fichier texte contenant votre message :

        ```bash
        echo "Message secret" > message.txt
        ```

5.  **Chiffrement du message**

    * Chiffrez le message à l'aide de la clé publique :

        ```bash
        openssl rsautl -encrypt -pubin -inkey public.pem -in message.txt -out message.enc
        ```

6.  **Visualisation du message chiffré**

    * Affichez le contenu du message chiffré (illisible) :

        ```bash
        cat message.enc
        ```

7.  **Déchiffrement du message**

    * Déchiffrez le message à l'aide de la clé privée :

        ```bash
        openssl rsautl -decrypt -inkey private.pem -in message.enc -out message.dec
        ```

8.  **Visualisation du message déchiffré**

    * Affichez le contenu du message déchiffré (en clair) :

        ```bash
        cat message.dec
        ```

## Explications

* `openssl genrsa` : Génère une paire de clés RSA.
* `openssl rsa` : Manipule les clés RSA (extraction de la clé publique).
* `openssl rsautl -encrypt` : Chiffre un fichier à l'aide d'une clé publique.
* `openssl rsautl -decrypt` : Déchiffre un fichier à l'aide d'une clé privée.
* `-pubin` : Indique que la clé d'entrée est une clé publique.
* `-inkey` : Spécifie le fichier contenant la clé.
* `-in` : Spécifie le fichier d'entrée.
* `-out` : Spécifie le fichier de sortie.

## Points importants

* Cette démonstration utilise des fichiers pour stocker les clés et les messages. En pratique, les clés doivent être stockées de manière plus sécurisée.
* La taille de la clé RSA (2048 bits) utilisée ici est une taille de clé standard.
* La commande `rsautl` est principalement utilisée pour des tests. Pour des données sensibles, il est préférable d'utiliser d'autres outils de chiffrement.

## Démo RSA 2:  Signature numérique avec RSA et OpenSSL

Cette démonstration vous guide à travers les étapes de création et de vérification d'une signature numérique à l'aide de l'algorithme RSA et de l'outil `openssl` sur Linux.

## Étapes

1.  **Génération des clés RSA**

    * Ouvrez un terminal et exécutez les commandes suivantes :

        ```bash
        openssl genrsa -out private.pem 2048
        openssl rsa -in private.pem -out public.pem -outform PEM -pubout
        ```

2.  **Création du document**

    * Créez un fichier texte représentant le document à signer :

        ```bash
        echo "Document à signer" > document.txt
        ```

3.  **Calcul du hachage du document**

    * Calculez le hachage SHA-256 du document :

        ```bash
        openssl dgst -sha256 -out document.hash document.txt
        ```

4.  **Signature du hachage avec la clé privée**

    * Signez le hachage avec la clé privée :

        ```bash
        openssl rsautl -sign -inkey private.pem -in document.hash -out document.signature
        ```

5.  **Vérification de la signature avec la clé publique**

    * Vérifiez la signature en déchiffrant le fichier de signature avec la clef publique, et en comparant le résultat avec le hash du document.

        ```bash
        openssl rsautl -verify -pubin -inkey public.pem -in document.signature -out document.hash.verification
        ```

    * Comparer le contenu des fichiers `document.hash` et `document.hash.verification` :

        ```bash
        diff document.hash document.hash.verification
        ```

    * Si la commande `diff` ne retourne rien, cela signifie que les deux fichiers sont identiques, et donc que la signature est valide.

## Explications

* `openssl dgst -sha256` : Calcule le hachage SHA-256 d'un fichier.
* `openssl rsautl -sign` : Signe un fichier à l'aide d'une clé privée.
* `openssl rsautl -verify` : Vérifie une signature à l'aide d'une clé publique.
* `diff` : Compare deux fichiers.

## Points importants

* La signature numérique garantit l'authenticité (l'auteur du document) et l'intégrité (le document n'a pas été modifié) du document.
* Le hachage est utilisé car il est plus efficace de signer un hachage qu'un document entier.
* La clé privée doit être conservée en sécurité, car elle permet de créer des signatures.
* La clé publique peut être diffusée librement, car elle permet uniquement de vérifier les signatures.
* Cette démonstration utilise SHA-256, mais d'autres algorithmes de hachage peuvent être utilisés.