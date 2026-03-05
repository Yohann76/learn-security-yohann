# Bcrypt (algorithme de hahchage de mots de passe robuste)

bcrypt est un algorithme de hachage de mots de passe spécialement conçu pour être résistant aux attaques par force brute. 
Il est largement recommandé pour le stockage sécurisé des mots de passe.

## Histoire et Origine

* **Création :** bcrypt a été conçu par Niels Provos et David Mazières et présenté lors de la conférence USENIX en 1999.
* **Objectif :** Il a été développé pour contrer les attaques par force brute contre les mots de passe hachés.

## Caractéristiques Clés

* **Hachage adaptatif :** bcrypt utilise un facteur de coût (cost factor) qui permet d'ajuster le temps de calcul nécessaire pour hacher un mot de passe.
* **Salage (salting) intégré :** Il génère et stocke un sel unique pour chaque mot de passe, ce qui rend les attaques par tables dictionnaire inefficaces.
* **Résistance aux attaques par force brute :** Sa conception le rend très résistant aux attaques par force brute, même avec des ordinateurs puissants ou des GPU.
* **Basé sur Blowfish :** bcrypt est basé sur l'algorithme de chiffrement Blowfish, modifié pour être une fonction de hachage à sens unique.

Blowfish est un algorithme de chiffrement symétrique par blocs. Blowfish est basé sur un réseau de Feistel, une structure couramment utilisée dans les algorithmes de chiffrement.

## Fonctionnement Interne

1.  **Génération du sel :** Un sel aléatoire est généré pour chaque mot de passe.
2.  **Hachage itératif :** Le mot de passe et le sel sont combinés et hachés de manière itérative, en utilisant l'algorithme Blowfish modifié.
3.  **Facteur de coût :** Le nombre d'itérations est contrôlé par le facteur de coût, qui détermine le temps de calcul nécessaire.
4.  **Stockage du hachage :** Le sel et le hachage résultant sont stockés ensemble.

## Avantages et Intérêts

* **Sécurité des mots de passe :** bcrypt est considéré comme l'un des algorithmes les plus sûrs pour le hachage de mots de passe.
* **Résistance aux attaques :** Il est résistant aux attaques par force brute, aux attaques par tables arc-en-ciel et aux attaques par compromission de la mémoire.
* **Adaptabilité :** Le facteur de coût permet d'adapter la sécurité aux capacités de calcul disponibles.

## Recommandations

* **Utiliser un facteur de coût élevé :** Il est recommandé d'utiliser un facteur de coût suffisamment élevé pour garantir une sécurité optimale.
* **Utiliser une bibliothèque de confiance :** Il est important d'utiliser une bibliothèque bcrypt de confiance pour éviter les vulnérabilités.
* **Mises à jour régulières :** Il est recommandé de mettre à jour régulièrement les bibliothèques bcrypt pour bénéficier des dernières améliorations de sécurité.