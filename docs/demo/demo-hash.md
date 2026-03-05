# Génération de hash 

sudo apt install hashcat openssl crunch whois 

## Générer un dictionnaire (de 2 caractéres, uniquement de chiffre)

crunch 2 2 0123456789 > custom_passwords.txt

echo -n "88" > password.txt

## Générer les fichiers password crypter dans différents algo

### MD5
openssl dgst -md5 password.txt | awk '{print $2}' > md5.hash

### SHA-1
openssl dgst -sha1 password.txt | awk '{print $2}' > sha1.hash

### SHA-256
openssl dgst -sha256 password.txt | awk '{print $2}' > sha256.hash

### SHA-512
openssl dgst -sha512 password.txt | awk '{print $2}' > sha512.hash

### bcrypt
mkpasswd --method=bcrypt 8888 > bcrypt.hash

### SHA-256 crypt (with salt)
openssl passwd -salt "$(openssl rand -base64 16)" -1 8888 > sha256_crypt.hash

### SHA-512 crypt (with salt)
openssl passwd -salt "$(openssl rand -base64 16)" -6 8888 > sha512_crypt.hash


## Test de bruteforce avec hashcat et mesure du temps (Ne fonctionne pas -> Manque de mémoire)

### MD5
time hashcat -m 0 md5.hash custom_passwords.txt

### SHA-1
time hashcat -m 100 sha1.hash custom_passwords.txt

### SHA-256
time hashcat -m 1400 sha256.hash custom_passwords.txt

### SHA-512
time hashcat -m 1700 sha512.hash custom_passwords.txt

### bcrypt
time hashcat -m 3200 bcrypt.hash custom_passwords.txt

### SHA-256 crypt
time hashcat -m 7300 sha256_crypt.hash custom_passwords.txt

### SHA-512 crypt
time hashcat -m 7400 sha512_crypt.hash custom_passwords.txt



