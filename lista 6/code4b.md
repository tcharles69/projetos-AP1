#include <stdio.h>

int main() {
    int avaliacao;

    printf("Digite um número de 1 a 5 (representando a avaliação): ");
    scanf("%d", &avaliacao);

    switch (avaliacao) {
        case 1:
            printf("Péssimo\n");
            break;
        case 2:
            printf("Ruim\n");
            break;
        case 3:
            printf("Médio\n");
            break;
        case 4:
            printf("Bom\n");
            break;
        case 5:
            printf("Excelente\n");
            break;
        default:
            printf("Erro: número inválido (deve ser entre 1 e 5).\n");
    }

    return 0;
}
