# Reverse Engineering (Autopsie d'un logiciel)

Le reverse engineering, ou rétro-ingénierie, est le processus qui consiste à analyser un système, un composant ou un logiciel pour en déterminer son fonctionnement interne, sa conception, son architecture ou son code source. 

C'est un peu comme démonter une montre pour comprendre comment elle fonctionne.

Différentes techniques pour démonter un systeme et comprendre son fonctionnement / lire un binaire etc.

**Pourquoi est-ce important en cybersécurité ?**

*   **Attaque :** Comprendre les mécanismes internes d'un logiciel permet de découvrir des vulnérabilités.
*   **Défense :** Analyser les logiciels malveillants (malwares) pour comprendre leur fonctionnement et créer des défenses efficaces.
*   **Audit de sécurité :** Vérifier la conformité d'un logiciel aux normes de sécurité et identifier les failles potentielles.

## Techniques de reverse engineering

Il existe différentes approches pour le reverse engineering, allant de l'analyse statique à l'analyse dynamique.

### 1. Analyse statique

*   **Description :** Examiner le code source (si disponible) ou le code binaire d'un logiciel sans l'exécuter.
*   **Outils :**
    *   **Désassembleurs :** Convertissent le code binaire en code assembleur (plus lisible). (Exemples : IDA Pro, Ghidra, radare2.)
    *   **Décompilateur :** Tentent de reconstruire le code source à partir du code binaire (plus difficile). (Exemples : JD-GUI (pour Java), .NET Reflector (pour .NET).)
    *   **Analyseurs de fichiers :** Aident à identifier le format des fichiers, les bibliothèques utilisées
    *   **Outils d'analyse de code :** Effectuent des analyses statiques pour détecter des vulnérabilités potentielles.
*   **Avantages :**
    *   Permet d'examiner le code en détail.
    *   Peut être effectuée sans risque d'infection.
*   **Inconvénients :**
    *   Peut être longue et fastidieuse.
    *   Difficile d'analyser les logiciels obfusqués ou protégés.
    *   Ne permet pas d'observer le comportement du logiciel en temps réel.

### 2. Analyse dynamique

*   **Description :** Exécuter le logiciel dans un environnement contrôlé (machine virtuelle) et observer son comportement.
*   **Outils :**
    *   **Débogueurs :** Permettent d'exécuter le code pas à pas, d'examiner la mémoire, et de modifier le comportement du logiciel. Exemples : OllyDbg, x64dbg, gdb.
    *   **Moniteurs système :** Enregistrent les activités du logiciel, comme les appels système, les accès aux fichiers et les communications réseau. Exemples : Process Monitor, Wireshark.
    *   **Analyseurs de mémoire :** Permettent d'examiner la mémoire du processus pour identifier des informations sensibles ou des structures de données intéressantes.
*   **Avantages :**
    *   Permet d'observer le comportement du logiciel en temps réel.
    *   Utile pour analyser les logiciels obfusqués ou protégés.
*   **Inconvénients :**
    *   Nécessite un environnement contrôlé pour éviter d'infecter le système hôte.
    *   Peut être difficile de reproduire certaines conditions d'exécution.
    *   Le logiciel peut détecter l'analyse dynamique et modifier son comportement.

### 3. Techniques combinées

*   Souvent, une combinaison d'analyse statique et dynamique est la plus efficace. L'analyse statique peut aider à identifier les zones intéressantes du code, tandis que l'analyse dynamique permet d'observer le comportement du logiciel lors de l'exécution.

## Applications du reverse engineering

*   **Analyse de logiciels malveillants :** Identifier le type de malware, son comportement, les données qu'il vole, et comment le neutraliser.
*   **Recherche de vulnérabilités :** Découvrir des failles de sécurité dans les logiciels pour pouvoir les corriger ou les exploiter.
*   **Développement d'exploits :** Créer des programmes qui exploitent les vulnérabilités pour prendre le contrôle d'un système.
*   **Analyse de protocoles :** Comprendre comment fonctionnent les protocoles de communication pour pouvoir les sécuriser ou les attaquer.
*   **Contournement de protections :** Déjouer les mécanismes de protection des logiciels, comme les systèmes de gestion des droits numériques (DRM).

## Défis du Reverse engineering

*   **Obfuscation :** Techniques pour rendre le code difficile à comprendre (renommage de variables, insertion de code inutile, etc.).
*   **Protection contre le débogage :** Méthodes pour empêcher le débogage du logiciel.
*   **Chiffrement :** Utilisation de techniques de chiffrement pour protéger le code ou les données.
*   **Code polymorphe :** Code qui change à chaque exécution pour éviter la détection.
*   **Complexité :** La taille et la complexité du code peuvent rendre le reverse engineering très difficile.

Le reverse engineering est une méthodequi peut être utilisé à des fins offensives et défensives en cybersécurité. 

Il nécessite des compétences techniques solides et une bonne connaissance des systèmes informatiques. 

**Voir démonstration reverse**