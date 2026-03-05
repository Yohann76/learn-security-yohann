# Demo iptables

Iptables n'est pas un pare-feu en soi, mais plutôt un outil de configuration pour le pare-feu intégré au noyau Linux, appelé netfilter. 

## Voir la politique de filtrage: 

sudo iptables -L -v --line-numbers

ping google.com (Montrer que ça fonctionne)

## Ajoutez la règle (bloquer les pings sortants)

La commande ping utilise des messages ICMP de type "echo request" (demande d'écho) pour tester la connectivité.

sudo iptables -A OUTPUT -p icmp --icmp-type echo-request -j DROP

Explication de la commande :
sudo iptables -A OUTPUT : Ajoute une règle à la chaîne OUTPUT (trafic sortant).
-p icmp : Spécifie le protocole ICMP.
--icmp-type echo-request : Spécifie le type de message ICMP "echo request" (demande d'écho).
-j DROP : Indique l'action à effectuer : bloquer le paquet.

ping google.com (voir aucun résultat)

sudo iptables -L -v --line-numbers // voir le numéro de ligne 
sudo iptables -D OUTPUT 1 // Supprimer la regle selon numéro de ligne (icmp echo-request)

L'ordre des règles est importante. iptables traite les règles de haut en bas et s'arrête à la première correspondance.

## Verbe d'action: 

ACCEPT :
Comportement :
    Autorise le paquet à passer.
    Le paquet est traité normalement par le système.
    Si le paquet est destiné à la machine locale, il est remis à l'application concernée.
    Si le paquet doit être transféré, il est routé vers sa destination.

2. DROP :
Comportement :
    Bloque le paquet silencieusement.
    Le paquet est supprimé sans envoyer de notification à l'expéditeur.
    L'expéditeur ne reçoit aucune indication que le paquet a été bloqué.
    C'est l'action la plus discrète.

3. REJECT :
Comportement :
    Bloque le paquet et envoie un message d'erreur à l'expéditeur.
    Le type de message d'erreur dépend du protocole (par exemple, ICMP pour les pings, TCP RST pour les connexions TCP).
    L'expéditeur est informé que le paquet a été bloqué.
    C'est une action moins discrète que DROP.

4. LOG :
Comportement :
    Enregistre les informations sur le paquet dans les journaux du système (par exemple, /var/log/syslog ou /var/log/messages).
    Le paquet continue d'être traité par les règles suivantes.
    Cette action est utile pour la surveillance et le dépannage.

5. RETURN :
Comportement :
    Arrête le traitement de la chaîne actuelle et retourne à la chaîne appelante.
    Si la règle est dans une chaîne intégrée (par exemple, INPUT, OUTPUT, FORWARD), le traitement continue avec la politique par défaut de cette chaîne.


----

# UFW (Uncomplicated Firewall)

sudo ufw status verbose // voir le status de ufw
sudo ufw allow ssh // Autoriser ssh pour éviter de se faire virer de son propre serveur 
sudo ufw enable // Utiliser ufw 
sudo ufw reload // recharger 
sudo ufw status verbose // verifier la config

ping google.com (voir le fonctionnement normal)

sudo nano /etc/ufw/before.rules // voir la liste des configuration

Ajoutez la ligne suivante avant la ligne COMMIT dans le fichier /etc/ufw/before.rules :
# Bloquer les pings sortants
-A ufw-before-output -p icmp --icmp-type echo-request -j DROP

sudo ufw reload

ping google.com (voir que ça ne fonctionne plus)

// Supprimer les ligne dans sudo nano /etc/ufw/before.rules

sudo ufw reload

ping google.com (voir que ça fonctionne)

sudo ufw disable // Desactiver car cela rend iptables non utilisable (car ufw est une couche supplémentaire de iptables)






