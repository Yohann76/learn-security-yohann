# Argon2 (hachage de mots de passe moderne et sécurisé)

Argon2 est un algorithme de hachage de mots de passe moderne et sécurisé, conçu pour être résistant aux attaques par force brute, aux attaques par dictionnaire. Il a été sélectionné comme gagnant du Password Hashing Competition en 2015.

## Histoire et Origine

* **Conception :** Argon2 a été conçu par Alex Biryukov, Daniel Dinu et Dmitry Khovratovich de l'Université du Luxembourg.
* **Objectif :** Il a été développé pour remplacer les algorithmes de hachage de mots de passe plus anciens, tels que bcrypt et scrypt, en offrant une meilleure protection contre les attaques modernes.

## Caractéristiques Clés

* **Résistance aux attaques par force brute :** Argon2 est conçu pour être lent et difficile à attaquer par force brute, même avec des ordinateurs puissants ou des GPU.
* **Résistance aux attaques par tables arc-en-ciel :** Il utilise un sel unique pour chaque mot de passe, ce qui rend les attaques par tables arc-en-ciel inefficaces.
* **Résistance aux attaques par compromission de la mémoire :** Argon2 est conçu pour être résistant aux attaques par compromission de la mémoire, qui consistent à voler les mots de passe hachés de la mémoire d'un ordinateur.
* **Trois variantes :** Argon2 comprend trois variantes :
    * **Argon2d :** Optimisé pour la résistance aux attaques par GPU.
    * **Argon2i :** Optimisé pour la résistance aux attaques par compromission de la mémoire.
    * **Argon2id :** Une combinaison des deux, offrant une bonne résistance aux deux types d'attaques.

## Fonctionnement Interne

1.  **Génération du sel :** Un sel aléatoire est généré pour chaque mot de passe.
2.  **Hachage itératif :** Le mot de passe et le sel sont combinés et hachés de manière itérative, en utilisant une fonction de hachage spéciale.
3.  **Paramètres de configuration :** Argon2 utilise trois paramètres de configuration :
    * **Temps de calcul (t) :** Le nombre d'itérations de hachage.
    * **Mémoire (m) :** La quantité de mémoire utilisée par l'algorithme.
    * **Parallélisme (p) :** Le nombre de threads utilisés pour le hachage.
4.  **Stockage du hachage :** Le sel, les paramètres de configuration et le hachage résultant sont stockés ensemble.

## Avantages et Intérêts

* **Sécurité des mots de passe :** Argon2 est considéré comme l'un des algorithmes les plus sûrs pour le hachage de mots de passe.
* **Résistance aux attaques :** Il est résistant à une large gamme d'attaques, y compris les attaques par force brute, les attaques par tables arc-en-ciel et les attaques par compromission de la mémoire.
* **Adaptabilité :** Les paramètres de configuration permettent d'adapter la sécurité aux capacités de calcul disponibles.

## Recommandations

* **Utiliser Argon2id :** Argon2id est la variante recommandée pour la plupart des applications.
* **Choisir des paramètres de configuration appropriés :** Il est important de choisir des paramètres de configuration qui offrent un bon équilibre entre sécurité et performance.
* **Utiliser une bibliothèque de confiance :** Il est important d'utiliser une bibliothèque Argon2 de confiance pour éviter les vulnérabilités.
* **Mises à jour régulières :** Il est recommandé de mettre à jour régulièrement les bibliothèques Argon2 pour bénéficier des dernières améliorations de sécurité.

**Voir démonstration hash**