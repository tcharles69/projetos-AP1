#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char str[100];
    char letra_substituir, nova_letra = '*';
    int i, j;

    // Leitura da string
    printf("Digite uma string: ");
    fgets(str, 100, stdin);

    // Remoção do caractere de nova linha
    str[strcspn(str, "\n")] = '\0';

    // Remoção dos espaços
    j = 0;
    for (i = 0; str[i]; i++) {
        if (str[i] != ' ') {
            str[j++] = str[i];
        }
    }
    str[j] = '\0';

    // Substituição da letra
    printf("Digite a letra a ser substituída: ");
    scanf("%c", &letra_substituir);

    for (i = 0; str[i]; i++) {
        if (tolower(str[i]) == tolower(letra_substituir)) {
            str[i] = nova_letra;
        }
    }

    // Exibição da string modificada
    printf("\nString modificada: %s\n", str);

}
