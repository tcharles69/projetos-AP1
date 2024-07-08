#include <stdio.h>

int main() {
    int numeros[12];
    int dobroNumeros[12];
    int i;

    // Leitura dos números
    printf("Digite 12 números inteiros:\n");
    for (i = 0; i < 12; i++) {
        printf("Número %d: ", i + 1);
        scanf("%d", &numeros[i]);
    }

    // Criação do novo vetor com o dobro de cada elemento
    for (i = 0; i < 12; i++) {
        dobroNumeros[i] = numeros[i] * 2;
    }

    // Impressão do novo vetor
    printf("O novo vetor é:\n");
    for (i = 0; i < 12; i++) {
        printf("%d ", dobroNumeros[i]);
    }
    printf("\n");
}
