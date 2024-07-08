#include <stdio.h>

#define QUANTIDADE_NUMEROS 5

int main() {
    float numeros[QUANTIDADE_NUMEROS];
    float soma = 0.0f;
    int i;

    // Leitura dos números
    printf("Digite %d números reais:\n", QUANTIDADE_NUMEROS);
    for (i = 0; i < QUANTIDADE_NUMEROS; i++) {
        printf("Número %d: ", i + 1);
        scanf("%f", &numeros[i]);
        soma += numeros[i];
    }

    // Cálculo da média
    float media = soma / QUANTIDADE_NUMEROS;

    // Impressão da média
    printf("A média dos números é: %.2f\n", media);

    return 0;
}
