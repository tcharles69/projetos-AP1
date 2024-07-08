#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {

    char palavra[100], palindromo[100];
    int i, igual = 0;

    printf("Digite uma palavra: ");
    scanf("%s", palavra);

    int tamanho = strlen(palavra);

    for(i = 0; i < tamanho; i++){
        palindromo[i] = palavra[tamanho - 1 - i];
    }
    palindromo[i] = '\0';

    printf("Original: %s\nInverso: %s\n", palavra, palindromo);

    for (i = 0; i < tamanho; i++){
        if(tolower(palavra[i]) == tolower(palindromo[i])){
            igual++;
        }
    }
    if(tamanho == igual){
        printf("%s eh palindroma\n", palavra);
    }else{
        printf("%s nao eh palindroma\n", palavra);
    }
}
