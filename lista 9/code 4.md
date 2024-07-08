#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char str[100];
    int i, j, vogais;

    // Leitura da string
    printf("Digite uma string: ");
    fgets(str, 100, stdin);

    // Remoção do caractere de nova linha
    str[strcspn(str, "\n")] = '\0';

    // Remoção das vogais
    j = 0;
    vogais = 0;
    for (i = 0; str[i]; i++) {
        if (tolower(str[i]) != 'a' && tolower(str[i]) != 'e' &&
            tolower(str[i]) != 'i' && tolower(str[i]) != 'o' &&
            tolower(str[i]) != 'u') {
            str[j++] = str[i];
        } else {
            vogais++;
        }
    }
    str[j] = '\0';

    // Exibição da string modificada
    printf("\nString modificada: %s\n", str);

    // Exibição do número de vogais
    printf("Número de vogais: %d\n", vogais);

}
