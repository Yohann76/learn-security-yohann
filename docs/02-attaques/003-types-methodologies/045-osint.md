# OSINT (Open Source Intelligence) : Le renseignement à sources ouvertes

Ce cours présente les principes fondamentaux de l'OSINT (Open Source Intelligence), ou renseignement à sources ouvertes. L'OSINT consiste à collecter et à analyser des informations accessibles au public pour produire du renseignement exploitable.

## Qu'est-ce que l'OSINT ?

L'OSINT se définit comme la collecte, le traitement et l'analyse d'informations accessibles au public (open sources) pour produire du renseignement exploitable. Ces sources comprennent :

*   **Internet** Sites web, blogs, forums, réseaux sociaux, moteurs de recherche, etc.
*   **Médias traditionnels** Journaux, magazines, radio, télévision.
*   **Publications gouvernementales** Rapports, documents, statistiques.
*   **Données commerciales** Annuaires d'entreprises, bases de données.
*   **Informations publiques** Bibliothèques, archives, conférences, etc.

L'OSINT ne se limite pas à la simple recherche d'informations. Elle implique également l'analyse, la validation et la contextualisation des données collectées pour en extraire du sens et produire du renseignement pertinent.

L'OSINT est de plus en plus importante dans de nombreux domaines :

*   **Cybersécurité:** Identification des menaces, analyse des vulnérabilités, surveillance des activités malveillantes (cf. Section 14 du `paste.txt` sur les vecteurs d'attaques).
*   **Enquêtes criminelles:** Recherche de preuves, identification de suspects, suivi des activités illégales.
*   **Sécurité nationale:** Surveillance des menaces terroristes, analyse des conflits, évaluation des risques.
*   **Renseignement économique:** Analyse de la concurrence, évaluation des marchés, identification des opportunités.
*   **Journalisme d'investigation:** Recherche d'informations, vérification des faits, révélation d'affaires publiques.

## Méthodologie OSINT

La méthodologie OSINT suit généralement les étapes suivantes :

1.  **Définition des objectifs:** Définir clairement les questions auxquelles l'OSINT doit répondre.
2.  **Identification des sources:** Identifier les sources d'informations pertinentes pour répondre aux questions.
3.  **Collecte des données:** Collecter les données à partir des sources identifiées.
4.  **Traitement des données:** Organiser, nettoyer et valider les données collectées.
5.  **Analyse des données:** Analyser les données pour identifier les tendances, les relations et les informations pertinentes.
6.  **Production du renseignement:** Rédiger un rapport de renseignement clair et concis, présentant les résultats de l'analyse et les conclusions.
7.  **Diffusion du renseignement:** Diffuser le rapport de renseignement aux personnes ou aux organisations concernées.

## Techniques OSINT

Il existe de nombreuses techniques OSINT, parmi lesquelles :

*   **Recherche avancée sur les moteurs de recherche:** Utiliser des opérateurs de recherche avancés (Google Dorking) pour affiner les requêtes et trouver des informations spécifiques.
*   **Analyse des réseaux sociaux:** Collecter des informations à partir des profils, des publications et des relations sur les réseaux sociaux.
*   **Géolocalisation:** Identifier la localisation géographique d'une personne, d'un objet ou d'un événement à partir de données disponibles en ligne.
*   **Analyse d'images et de vidéos:** Extraire des informations à partir d'images et de vidéos (métadonnées, objets, lieux).
*   **Analyse de données massives (Big Data):** Utiliser des outils d'analyse de données pour traiter et analyser de grandes quantités d'informations.

### Google Dorking

Le Google Dorking, aussi appelé "Google hacking", consiste à utiliser des opérateurs de recherche avancés dans Google (ou d'autres moteurs de recherche) pour trouver des informations spécifiques qui ne sont pas facilement accessibles via une recherche simple.

*   **Opérateurs de recherche courants:**
  *   `site:` : Limiter la recherche à un site web spécifique (ex: `site:example.com`).
  *   `filetype:` : Rechercher des fichiers d'un type spécifique (ex: `filetype:pdf`).
  *   `intitle:` : Rechercher des pages web dont le titre contient un mot clé spécifique (ex: `intitle:"index of"`).
  *   `inurl:` : Rechercher des pages web dont l'URL contient un mot clé spécifique (ex: `inurl:admin`).
  *   `ext:` : Similaire à `filetype:`, mais plus court (ex: `ext:doc`).

*   **Exemples de requêtes Google Dorking:**
  *   `site:example.com filetype:pdf "rapport confidentiel"` : Trouver des rapports confidentiels au format PDF sur le site example.com.
  *   `intitle:"index of" "motdepasse.txt"` : Trouver des répertoires indexés contenant des fichiers nommés "motdepasse.txt".

**Attention:** L'utilisation de Google Dorking pour accéder à des informations non autorisées peut être illégale. Il est important de respecter les lois et les règles d'éthique lors de l'utilisation de ces techniques.

## Outils OSINT

Il existe de nombreux outils OSINT disponibles, gratuits ou payants. Voici quelques exemples :

*   **Recherche:**
  *   Google : Le moteur de recherche le plus utilisé.
  *   DuckDuckGo : Un moteur de recherche axé sur la confidentialité.
  *   Shodan : Un moteur de recherche pour les appareils connectés à Internet.
*   **Analyse de données:**
  *   Google Dataset Search : un moteur de recherche pour les ensembles de données
*   **Frameworks OSINT:**
  *   OSINT Framework ([OSINT Framework](https://osintframework.com/)): ce framework est une page web contenant de nombreux liens vers des outils OSINT. Il est organisé par catégories (noms d'utilisateur, adresses e-mail, réseaux sociaux, etc.).

## Références:

*  [YT: Trouver un endroit à partir d'une image](https://www.youtube.com/watch?v=udYtHVEwbYA)
*  [YT: Exemple outils OSINT](https://www.youtube.com/watch?v=qz5lSFS4BYY)
*  [Game OSINT](https://sourcing.games/#games)