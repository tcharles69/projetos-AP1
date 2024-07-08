#include <stdio.h>


int main() {
    int numero[10];
    int i, numeroEscolhido, numeroIgual = 0,posicao = -1;

    // Leitura dos números
    printf("Digite 10 números inteiros:\n");
    for (i = 0; i < 10; i++) {
        printf("Número %d: ", i + 1);
        scanf("%d", &numero[i]);
    }

    // Solicitação do número a ser procurado
    printf("Digite o número que você deseja procurar: ");
    scanf("%d", &numeroEscolhido);

    // Procurando o número no vetor
    for (i = 0; i < 10; i++) {
        if (numero[i] == numeroEscolhido) {
           numeroIgual = 1;
           posicao = i;
           break;
        }
    }

    // Impressão do resultado
    if (numeroIgual) {
        printf("O número %d foi encontrado na posição %d.\n", numeroEscolhido, posicao);
    } else {
        printf("O número %d não foi encontrado no vetor.\n", numeroEscolhido);
    }

    return 0;
}
