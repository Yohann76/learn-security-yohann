# Demo reverse 

// Installer un compilateur C et un outils de desassemblage (objdump)
sudo apt install gcc binutils

// Créer un programme en C 

echo '#include <stdio.h>

int main() {
    printf("Bonjour, le monde !\n");
    return 0;
}
' > hello.c

// Compiler en C: 

gcc hello.c -o hello

// Voir le code compilé 
cat hello

// Utiliser dump pour déssassembler 
objdump -d hello // affiche les infos principale et fonctions
objdump -s hello // affiche le details de toute les sections // on peux voir la chaine de caractére




// Utiliser un autre logiciel: 

sudo apt install gdb

gdb ./hello   // lancer GDB  avec l'executable hello
info functions // pour voir les fonction
disassemble main  // par convention, tout les programmes en C ont une fonction main

x/s 0x2004 // Trouver la chaine "Bonjour le monde"  // eXamine la mémoire à l'adresse 0x2004 et interprète-la comme une String (chaîne de caractères) en C  // x(examine) la mémoire 0x2004 sous forme de chaine de caractére

exit


