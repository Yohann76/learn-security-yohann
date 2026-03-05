# Les différentes vulnérabilitées

## C'est quoi une vulnérabilité ? 

Une vulnérabilité est une faiblesse dans un système d'information (logiciel, matériel, configuration réseau, etc.) qui peut être exploitée par une menace pour compromettre la confidentialité, l'intégrité ou la disponibilité de ce système. En d'autres termes, c'est une faille de sécurité qui peut être utilisée pour réaliser une attaque.

Les vulnérabilités peuvent être dues à des erreurs de conception, des erreurs de programmation, des configurations incorrectes ou des composants obsolètes.

## OWASP10 

L'OWASP (Open Web Application Security Project) est une organisation à but non lucratif qui travaille à améliorer la sécurité des logiciels. L'un de ses projets les plus connus est l'OWASP Top 10, une liste des dix vulnérabilités les plus critiques pour les applications web.

*   **Description :** L'OWASP Top 10 est une liste de sensibilisation, conçue pour aider les développeurs, les architectes, les testeurs et les responsables de la sécurité à comprendre les risques les plus courants pour les applications web.
*   **Liste 2021 :**
    1.  Injection
    2.  Broken Authentication
    3.  Sensitive Data Exposure
    4.  XML External Entities (XXE)
    5.  Broken Access Control
    6.  Security Misconfiguration
    7.  Cross-Site Scripting (XSS)
    8.  Insecure Deserialization
    9.  Using Components with Known Vulnerabilities
    10. Insufficient Logging & Monitoring
*   **Plus d'informations :** Vous pouvez consulter la liste complète et les détails de chaque vulnérabilité sur le site de l'OWASP : [OWASP10](https://owasp.org/www-project-top-ten/)

## 0-days (Zero-Day Exploits)

*   **Définition :** Une vulnérabilité "0-day" (ou "zero-day") est une vulnérabilité qui est inconnue du fournisseur du logiciel ou du matériel concerné. Cela signifie qu'il n'existe pas encore de correctif disponible pour corriger cette vulnérabilité.
*   **Danger :** Les vulnérabilités 0-day sont particulièrement dangereuses car elles peuvent être exploitées par des attaquants avant que les défenseurs ne puissent prendre des mesures pour se protéger.
*   **Marché :** Il existe un marché noir des vulnérabilités 0-day, où des chercheurs en sécurité (ou des personnes mal intentionnées) vendent des informations sur ces vulnérabilités à des gouvernements, des entreprises ou des cybercriminels.

## Comment découvrir une vulnérabilité ?

La découverte de vulnérabilités est un domaine complexe qui nécessite des compétences techniques, de la patience et de la persévérance. Voici quelques approches courantes :

1.  **Analyse statique du code :** Examiner le code source d'un logiciel à la recherche de potentielles failles de sécurité (erreurs de logique, buffer overflows, etc.).
2.  **Analyse dynamique :** Exécuter le logiciel et tester différents scénarios pour identifier des comportements anormaux ou des erreurs. Cela peut inclure du fuzzing (injection de données aléatoires pour provoquer des erreurs).
3.  **Reverse engineering :** Décompiler un logiciel pour analyser son fonctionnement interne et identifier des vulnérabilités.
5.  **Veille sur les nouvelles technologies :** Se tenir informé des nouvelles technologies et des nouvelles vulnérabilités découvertes.
6.  **Tests d'intrusion (pentesting) :** Simuler des attaques pour évaluer la sécurité d'un système.

## Nommage des vulnérabilités (CVE)

### CVE et MITRE 

*   **CVE :** CVE (Common Vulnerabilities and Exposures) est un système de nommage standardisé pour les vulnérabilités de sécurité informatique. Chaque vulnérabilité reçoit un identifiant CVE unique, ce qui permet de faciliter la communication et le partage d'informations sur les vulnérabilités.
*   **Format :** Les identifiants CVE ont le format suivant : CVE-YYYY-NNNN (où YYYY est l'année de découverte de la vulnérabilité et NNNN est un numéro).
*   **Objectif :** Le système CVE permet aux professionnels de la sécurité, aux fournisseurs de logiciels et aux utilisateurs de parler de la même vulnérabilité sans ambiguïté.
*   **Plus d'informations :** Vous pouvez consulter la base de données CVE sur le site du MITRE : [CVE MITRE](https://cve.mitre.org/)

**L'organisation MITRE (The MITRE Corporation)** est une organisation à but non lucratif qui gère plusieurs centres de recherche et développement financés par le gouvernement fédéral américain (FFRDC). MITRE travaille dans l'intérêt public, en fournissant une expertise dans des domaines variés tels que l'aviation, la cybersécurité, la santé, la sécurité intérieure et la défense. Bien que MITRE intervienne dans de nombreux domaines, elle est particulièrement reconnue dans le monde de la cybersécurité.

## Le rôle de MITRE

*   **Gestion du programme CVE :** MITRE est responsable de la gestion globale du programme CVE. Elle définit les politiques et les procédures pour l'attribution des numéros CVE, forme et certifie les CNA, et maintient la liste CVE principale.
*   **Attribution de CVE en dernier recours :** Si une vulnérabilité ne relève pas de la compétence d'une CNA existante, MITRE peut attribuer directement un numéro CVE.
*   **Publication et maintenance de la base de données CVE :** MITRE publie et maintient la base de données CVE, qui contient des informations sur toutes les vulnérabilités CVE connues.

# Attribution des numéros CVE : Qui fait quoi ?

Il est courant de penser que MITRE attribue directement tous les numéros CVE, mais la réalité est un peu plus nuancée. Voici une explication plus précise :

### Les CNA (CVE Numbering Authorities)

*   **Définition :** Les CNA (CVE Numbering Authorities) sont des organisations autorisées à attribuer des numéros CVE aux vulnérabilités qu'elles découvrent ou qui leur sont signalées. Ce sont des partenaires de MITRE.
*   **Rôle :** Les CNA agissent comme des points de contact pour la divulgation des vulnérabilités. Elles analysent les vulnérabilités, déterminent si elles répondent aux critères CVE et, si c'est le cas, leur attribuent un numéro CVE.
*   **Types de CNA :** Les CNA peuvent être des fournisseurs de logiciels, des organisations de recherche en sécurité, des CERT (Computer Emergency Response Teams) ou d'autres organisations impliquées dans la gestion des vulnérabilités.
*   **Exemples de CNA :** Microsoft, Google, Cisco, Red Hat, CERT/CC (Carnegie Mellon University), etc.

### Autres systèmes de nommage et de classification

Bien que CVE soit le système le plus largement utilisé, il existe d'autres approches pour nommer et classer les vulnérabilités :

*   **CVSS (Common Vulnerability Scoring System) :**
  *   **Description:** CVSS n'est pas un système de nommage, mais plutôt un système d'évaluation de la gravité des vulnérabilités. Il est souvent utilisé en conjonction avec les identifiants CVE.
  *   **Objectif:** Fournir une méthode standardisée pour évaluer la gravité d'une vulnérabilité, en tenant compte de différents facteurs tels que l'exploitabilité, l'impact sur la confidentialité, l'intégrité et la disponibilité.
  *   **Plus d'informations:** [https://www.first.org/cvss/](https://www.first.org/cvss/)
*   **CWE (Common Weakness Enumeration) :**
  *   **Description:** CWE est un système de classification des *types* de faiblesses logicielles (par exemple, "buffer overflow", "injection SQL").
  *   **Objectif:** Fournir un langage commun pour décrire les faiblesses logicielles, afin d'aider les développeurs à écrire du code plus sûr et les outils de sécurité à détecter ces faiblesses.
  *   **Plus d'informations:** [CVE MITRE](https://cwe.mitre.org/)
*   **Bugtraq ID :**
  *   **Description:** Identifiants utilisés par la liste de diffusion Bugtraq (aujourd'hui moins active) pour référencer les vulnérabilités.
*   **Vendor-Specific IDs :**
  *   **Description:** Identifiants propres aux fournisseurs de logiciels (par exemple, Microsoft utilise des identifiants de la forme "MS##-NNN").

## Que faire si je trouve une vulnérabilité sur internet ?

Si vous découvrez une vulnérabilité sur un site web, une application ou un logiciel, il est important de suivre une procédure responsable et éthique :

1.  **Ne pas exploiter la vulnérabilité :** Il est illégal et contraire à l'éthique d'exploiter une vulnérabilité sans autorisation. Ne tentez pas d'accéder à des données sensibles, de modifier des systèmes ou de causer des dommages.
2.  **Identifier le propriétaire du système :** Essayez de déterminer qui est responsable du système vulnérable (entreprise, organisation, particulier).
3.  **Contacter le propriétaire :** Contactez le propriétaire du système et informez-le de la vulnérabilité que vous avez découverte. Fournissez-lui des informations détaillées sur la vulnérabilité, y compris les étapes pour la reproduire et les preuves de concept (sans toutefois exploiter activement la vulnérabilité).
4.  **Laisser un délai raisonnable :** Donnez au propriétaire du système un délai raisonnable pour corriger la vulnérabilité. Ce délai peut varier en fonction de la gravité de la vulnérabilité et des ressources du propriétaire.
5.  **Divulgation responsable (Responsible Disclosure) :** Si le propriétaire du système ne répond pas ou ne corrige pas la vulnérabilité dans un délai raisonnable, vous pouvez envisager de divulguer publiquement la vulnérabilité. Cependant, il est important de le faire de manière responsable et en coordination avec le propriétaire du système.
6.  **Bug bounty programs :** Si le système vulnérable fait partie d'un programme de récompenses de bugs, vous pouvez signaler la vulnérabilité via ce programme.

**Ressources importantes :**

*   **CERT (Computer Emergency Response Team) :** Si vous ne parvenez pas à contacter le propriétaire du système ou si la vulnérabilité est critique, vous pouvez contacter le CERT de votre pays. Le CERT est une organisation chargée de la gestion des incidents de sécurité informatique.
  *   **CERT-FR (France) :** [https://www.cert.ssi.gouv.fr/](https://www.cert.ssi.gouv.fr/)
  *   **Autres CERT :** Vous trouverez une liste des CERT nationaux sur le site de FIRST : [https://www.first.org/members/map](https://www.first.org/members/map)
*   **Signalement de vulnérabilités :** De nombreuses plateformes et organisations proposent des formulaires de signalement de vulnérabilités. Faites une recherche en ligne pour trouver la plateforme appropriée pour le système vulnérable que vous avez découvert.

**Important :** La divulgation publique d'une vulnérabilité avant qu'elle ne soit corrigée peut mettre en danger de nombreuses personnes et organisations. Il est donc essentiel de suivre une procédure responsable et éthique.

 

