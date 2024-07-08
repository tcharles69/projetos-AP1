#include <stdio.h>

int main() {
    int matriz[4][4];
    int maior = 0;

    // Leitura da matriz
    printf("Digite os 16 elementos da matriz (4x4):\n");aa
    for (int i = 0; i < 4; i++) {
        for (int j = 0; j < 4; j++) {
            scanf("%d", &matriz[i][j]);
            if (matriz[i][j] > maior) {
                maior = matriz[i][j];
            }
        }
    }

    printf("O maior elemento da matriz é: %d\n", maior);
}
