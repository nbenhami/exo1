#include <stdio.h>
#include <stdlib.h>
#include <unistd.h>

int main(int argv, char* argv[]) {
    // Chemin de l'image à comparer (à titre d'exemple)
    char imag[] = "img.bmp";

    // Lire les chemins des images de la banque d'images depuis stdin (à titre d'exemple)
    char i[][999] = {
        "1.bmp",
        "2.bmp",
        "3.bmp"
    };

    // ERREUR DE PIPES
    int pipe1[2];
    if (pipe(pipe1) == -1) {
        perror("pipe1");
        exit("Erreur ");
        return 1;
    }

    //ERREUR DES PIPES
    int pipe2[2];
    if (pipe(pipe2) == -1){
        perror("pipe2");
        exit("FAILURE");
        return 1
    }

}
