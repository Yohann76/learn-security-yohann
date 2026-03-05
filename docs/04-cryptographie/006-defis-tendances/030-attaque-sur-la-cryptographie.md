# Attaques contre la cryptographie

La cryptographie, bien qu'essentielle pour la sécurité des données, n'est pas infaillible. 
Différentes attaques peuvent être utilisées pour tenter de compromettre les systèmes cryptographiques (Ou seulement observer des communications).

## Attaques par Force Brute

* **Principe :** Essayer toutes les combinaisons possibles de clés jusqu'à trouver la bonne.
* **Vulnérabilité :** Les clés courtes sont plus vulnérables. La puissance de calcul croissante rend cette attaque de plus en plus efficace.
* **Contre-mesures :** Utiliser des clés suffisamment longues et des algorithmes de hachage lents.

*  **Principe de fonctionnement**
  *  L'attaquant essaie systématiquement toutes les combinaisons possibles de caractères, de chiffres ou de symboles, jusqu'à ce qu'il trouve la bonne clé ou le bon mot de passe.
  *  C'est comme essayer toutes les combinaisons d'un cadenas à chiffres jusqu'à ce qu'il s'ouvre.
  *  La complexité de l'attaque dépend de la longueur et de la complexité de la clé ou du mot de passe.

## Attaques par Dictionnaire

* **Principe :** Essayer des mots de passe courants ou des variations de ceux-ci.
* **Vulnérabilité :** Les mots de passe faibles sont très vulnérables.
* **Contre-mesures :** Encourager l'utilisation de mots de passe forts et uniques.

*  Contrairement à une attaque par force brute qui essaie toutes les combinaisons possibles, une attaque par dictionnaire se concentre sur les mots de passe les plus probables.
*  Dans le cadre d'attaque sur la cryptographie, l'attaquant va souvent récupérer des bases de données de hash de mots de passe, et les comparer aux hashs de son dictionnaire.

## Attaques par Collision

* **Principe :** Trouver deux entrées différentes produisant le même hachage.
* **Vulnérabilité :** Certains algorithmes de hachage sont plus vulnérables aux collisions.
* **Contre-mesures :** Utiliser des algorithmes de hachage résistants aux collisions (SHA-256, SHA-3).

*  **Scénario**
  *  Un cybercriminel crée deux documents PDF.
  *  Le premier document est un contrat légitime.
  *  Le deuxième document est un contrat frauduleux, avec des clauses modifiées à l'avantage du cybercriminel.
  *  Le cybercriminel utilise une attaque par collision pour s'assurer que les deux documents produisent le même hachage MD5.
  *  Il présente le document légitime à sa victime, qui le signe numériquement.
  *  Le cybercriminel remplace ensuite le document légitime par le document frauduleux, qui conserve la signature numérique valide.
  *  La victime ce retrouve donc avec un document signé, prouvant un contrat qu'elle n'a jamais voulu.

## Attaques par Canal Latéral

Les attaques par canal latéral exploitent les informations divulguées par l'implémentation physique des algorithmes cryptographiques, telles que la consommation d'énergie, le temps d'exécution ou les émissions électromagnétiques.

Imaginez que vous essayez de deviner un code PIN à 4 chiffres en observant une personne le saisir sur un clavier. Au lieu de regarder directement les chiffres, vous écoutez attentivement les sons produits par chaque touche. Vous remarquez que certaines touches émettent un son légèrement différent, ou que le temps entre les pressions varie. Ces subtilités sont des "canaux latéraux" d'information.

En cryptographie, les attaques par canal latéral fonctionnent de manière similaire. Au lieu d'attaquer la robustesse mathématique d'un algorithme de chiffrement, elles exploitent les informations physiques qui "fuient" pendant son exécution.

* **Vecteurs d'attaque:**
  *  Consommation d'énergie
  *  Temps d'exécution
  *  Émissions électromagnétiques
  *  Émissions acoustiques 
  *  Émissions de lumière des composants
  *  Température
  *  Analyse de cache (et de sa performance)

* **Exemple:**
  *  Scénario : Une carte à puce effectue un calcul de chiffrement RSA. Chaque opération (multiplication, exponentiation) consomme une quantité d'énergie légèrement différente.
  *  Attaque : Un attaquant mesure la consommation électrique de la carte pendant le calcul. 
     En analysant les variations de consommation, il peut déduire quelles opérations ont été effectuées et dans quel ordre.
  *  Résultat : L'attaquant peut reconstruire les étapes du calcul et, potentiellement, extraire la clé privée utilisée pour le chiffrement.

*   **Risques :** Ces attaques peuvent permettre aux attaquants d'extraire des clés ou d'obtenir des informations sur le fonctionnement interne des algorithmes.

### Solutions

*   **Contre-Mesures Matérielles :** Utilisation de dispositifs matériels conçus pour minimiser les fuites d'informations par canal latéral. 
    (Entourer les composants sensibles d'un blindage   électromagnétique pour réduire les émissions.)
*   **Contre-Mesures Logicielles :** Mise en œuvre d'algorithmes cryptographiques résistants aux attaques par canal latéral, tels que le masquage et le brassage.

*  **Masquage:** Ajouter du bruit aléatoire aux mesures de consommation électrique pour rendre l'analyse plus difficile.
*  **Brassage :** Modifier l'ordre des opérations pour rendre l'analyse de consommation plus complexe.
*  **Algorithmes à temps constant :** Concevoir des algorithmes dont le temps d'exécution est indépendant des données traitées.


## Attaques par Ingénierie Sociale

* **Principe :** Manipuler les utilisateurs pour obtenir des informations sensibles.
* **Vulnérabilité :** Les utilisateurs sont souvent le maillon faible de la sécurité.
* **Contre-mesures :** Sensibiliser les utilisateurs aux risques d'ingénierie sociale.



La cryptographie est un domaine en constante évolution, et de nouvelles attaques sont découvertes régulièrement. Il est essentiel de rester informé des dernières vulnérabilités et de mettre en œuvre des contre-mesures appropriées pour protéger les systèmes cryptographiques.