
# Mon OS 🚀

<!-- Ici, tu peux mettre un petit badge (ex: "Statut: en développement") -->

> Un petit système d'exploitation créé de zéro pour apprendre la programmation système.

Ce projet est le fruit de mon apprentissage du langage **C**, de la **gestion de la mémoire** et des bases de l'**assembleur**. L'objectif est de comprendre comment un ordinateur démarre et comment un noyau (kernel) interagit avec le matériel.

## 🧠 Pourquoi ce projet ?

J'ai voulu dépasser le code "classique" pour comprendre ce qui se passe vraiment sous le capot d'une machine. [citation:1] En construisant ce mini-OS, j'ai appris :
*   À écrire un bootloader en assembleur x86.
*   Le passage d'un processeur du mode 16 bits au mode 32 bits.
*   À manipuler la mémoire vidéo (VGA) pour afficher du texte en C.
*   Les bases de la compilation croisée et de l'émulation avec QEMU.

## ⚙️ Fonctionnalités actuelles

- ✅ Bootloader fonctionnel qui charge le noyau.
- ✅ Affichage de texte en mode VGA.
- ✅ Gestion basique des interruptions.
- ⚙️ [En cours] Gestion de la mémoire (`kmalloc`).
- 🔜 [Prévu] Support du clavier.

## 🚀 Comment le lancer ?

### Prérequis
- **WSL2** (si tu es sur Windows) ou un environnement Linux.
- **NASM** (assembleur) : `sudo apt install nasm`
- **QEMU** (émulateur) : `sudo apt install qemu-system-x86`
- **GCC** (compilateur C) : `sudo apt install gcc`

### Étapes
1.  Clone le dépôt sur ta machine :

2.  Assemble le bootloader :
nasm -f bin boot.asm -o boot.bin
3. Compile le noyau :gcc -m32 -ffreestanding -nostdlib -c kernel.c -o kernel.o
# (Le lien du noyau sera ajouté plus tard)
4. Lance le système dans QEMU :

qemu-system-x86_64 -fda boot.bin
5. 
6. 



    ```bash
    git clone https://github.com/TON-COMPTE/Mon-OS.git
    cd Mon-OS
