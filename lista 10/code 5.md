#include <stdio.h>

int main() {
    int matriz[3][3];
    int maior = 0;

    printf("Digite os 9 elementos da matriz (3x3):\n");
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            scanf("%d", &matriz[i][j]);
        }
    }

    printf("Matriz organizada:\n");
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            printf("[%d] ", matriz[i][j]);
        }
        printf("\n");
    }
}
