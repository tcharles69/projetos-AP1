#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char frase[100];
    int i, palavras, caracteres;

    // Leitura da frase
    printf("Digite uma frase: ");
    fgets(frase, 100, stdin);

    // Remoção do caractere de nova linha
    frase[strcspn(frase, "\n")] = '\0';

    // Contagem de palavras
    palavras = 1;
    for (i = 0; frase[i]; i++) {
        if (frase[i] == ' ') {
            palavras++;
        }
    }

    // Contagem de caracteres
    caracteres = strlen(frase);

    // Exibição da frase em maiúsculas
    printf("\nFrase em maiúsculas: ");
    for (i = 0; frase[i]; i++) {
        putchar(toupper(frase[i]));
    }
    printf("\n");

    // Exibição da frase em minúsculas
    printf("Frase em minúsculas: ");
    for (i = 0; frase[i]; i++) {
        putchar(tolower(frase[i]));
    }
    printf("\n");

    // Exibição do número de palavras e caracteres
    printf("\nNúmero de palavras: %d\n", palavras);
    printf("Número de caracteres: %d\n", caracteres);

}
