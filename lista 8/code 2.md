#include <stdio.h>

int main() {
    int numeros[8];
    int i, max, min;

    // Leitura dos números
    printf("Digite 8 números inteiros:\n");
    for (i = 0; i < 8; i++) {
        printf("Número %d: ", i + 1);
        scanf("%d", &numeros[i]);
    }

    // Encontrando o maior e o menor elemento
    max = numeros[0];
    min = numeros[0];
    for (i = 1; i < 8; i++) {
        if (numeros[i] > max) {
            max = numeros[i];
        }
        if (numeros[i] < min) {
            min = numeros[i];
        }
    }

    // Impressão do maior e do menor elemento
    printf("O maior elemento é: %d\n", max);
    printf("O menor elemento é: %d\n", min);

    return 0;
}
