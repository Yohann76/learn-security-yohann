## TP Vulnérabilité sur des modéles de données (IA): 

[TP: attaque sur IA](https://gandalf.lakera.ai/baseline)

La sécurité des modèles d'IA est un domaine en pleine expansion, car les modèles sont de plus en plus utilisés dans des applications critiques.

*  Technique pour chercher une vulnérabilité: 
  *  **Injection de prompt directe :** Consiste à insérer des instructions malveillantes directement dans le prompt pour contourner les restrictions du modèle. Par exemple, on pourrait essayer d'ajouter des commandes spécifiques qui modifient le comportement de l'IA.
  *  **Injection de prompt indirecte :** Implique l'intégration d'instructions malveillantes dans des sources externes comme des fichiers ou des sites web, qui sont ensuite traités par l'IA. Ces instructions peuvent être invisi*bles pour l'humain mais lisibles par le modèle.
  *  **Incitation à la chaîne de pensée:** Encourage l'IA à décomposer son raisonnement en étapes logiques, ce qui peut révéler des informations supplémentaires sur son processus de réflexion.
  *  **Incitation par exemples:** Fournit quelques exemples pertinents dans le prompt pour guider l'IA vers le type de réponse souhaité, potentiellement en l'orientant vers des informations sensibles.
  *  **Attaques indirectes progressives:** Influence le comportement du système d'IA au fil du temps en insérant des prompts malveillants qui modifient subtilement le contexte pour affecter les réponses futures.
  *  **Techniques automatisées:** Des méthodes plus avancées, comme celles développées par des chercheurs, utilisent des approches automatisées basées sur des concepts mathématiques pour générer des prompts qui maximisent la probabilité d'obtenir des réponses non filtrées