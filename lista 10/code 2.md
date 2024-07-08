#include <stdio.h>

int main() {
    int matriz[3][3];
    int numero;
    int encontrado = 0;

    // Leitura da matriz
    printf("Digite os 9 elementos da matriz (3x3):\n");
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            scanf("%d", &matriz[i][j]);
        }
    }

    // Leitura do número a ser procurado
    printf("Digite o número a ser procurado: ");
    scanf("%d", &numero);

    // Verificação da presença do número na matriz
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            if (matriz[i][j] == numero) {
                encontrado = 1;
                printf("O número %d está presente na matriz.\n", numero);
                break;
            }
        }
        if (encontrado) {
            break;
        }
    }

    if (!encontrado) {
        printf("O número %d não está presente na matriz.\n", numero);
    }
}
