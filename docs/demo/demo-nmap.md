# demo nmap (Outils de scan)

`scanme.nmap.org` est un site spécialement configuré pour permettre aux utilisateurs de tester et d'apprendre à utiliser Nmap. 
*C'est une cible légale et sûre pour pratiquer vos compétences en matière de scan de réseau.

sudo apt install nmap

nmap scanme.nmap.org (Cette commande effectuera un scan TCP SYN par défaut, qui tente d'établir une connexion TCP avec les ports les plus courants.)
nmap -sV scanme.nmap.org (Voir les versions des services en cours)
nmap -O scanme.nmap.org (Detection de l'OS cible)
nmap -sS -sV -sC scanme.nmap.org (Scan plus approfondie)

On peux voir le port 80, utilise une version de Apache httpd 2.4.7
Et donc rechercher les vulnérabilitées connus sur ce service:
[CVE Details](https://www.cvedetails.com/vendor/45/)
[exploit-db](https://www.exploit-db.com/)

## Analyser les sous domaines

[crt sh](https://crt.sh/)

Avec un outils (sublist3r): 

sudo apt install python3-pip
sudo pip3 install sublist3r
sublist3r -d boldcode.io // (-d pour la cible)

## Autre analyse

### Installation et explication
sudo apt install -y nmap netcat-traditional dnsutils whois traceroute

nmap : Scanner de réseau pour découvrir des hôtes, des services.
netcat-traditional : Outil polyvalent pour lire des données sur des connexions réseau 
dnsutils : Utilitaires DNS pour interroger les serveurs DNS (résoudre des noms de domaine)
whois : Interroger les bases de données WHOIS pour obtenir des informations sur le propriétaire d'un domaine ou d'une adresse IP
traceroute : Afficher le chemin suivi par les paquets pour atteindre une cible (identifier les routeurs, visualiser la topologie réseau)

### Commande: 

sudo apt install -y nmap netcat-traditional dnsutils whois traceroute
ping -c 4 scanme.nmap.org // Verifier que c'est accessible -> peux donner une idée de la distance du réseaux
traceroute scanme.nmap.org // Affiche le chemin de la requéte // identifier les routeurs traversés / Peut révéler la localisation géographique approximative du serveur
dig NS boldcode.io // scan avec pour les serveurs de noms 
whois google.com // Affiche des informations sur le propriétaire du domaine (peuvent être masquées)





