#include <stdio.h>

int main() {
    float matriz[3][4];
    float media[3];

    printf("Digite as 12 notas (4 notas para cada aluno):\n");
    for (int i = 0; i < 3; i++) {
        printf("Aluno %d:\n", i + 1);
        for (int j = 0; j < COLS; j++) {
            scanf("%f", &matriz[i][j]);
        }
    }

    for (int i = 0; i < 3; i++) {
        float soma = 0.0;
        for (int j = 0; j < 4; j++) {
            soma += matriz[i][j];
        }
        media[i] = soma / 4;
    }

    printf("\nMédias dos alunos:\n");
    for (int i = 0; i < 3; i++) {
        printf("Aluno %d: %.2f\n", i + 1, media[i]);
    }
}
