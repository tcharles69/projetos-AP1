#include <stdio.h>

int main() {
    char op;
    float num1, num2, result;

    printf("Digite a operação matemática (+, -, *, /): ");
    scanf("%c", &op);

    printf("Digite o primeiro número: ");
    scanf("%f", &num1);

    printf("Digite o segundo número: ");
    scanf("%f", &num2);

    switch (op) {
        case '+':
            result = num1 + num2;
            printf("Resultado: %.2f\n", result);
            break;
        case '-':
            result = num1 - num2;
            printf("Resultado: %.2f\n", result);
            break;
        case '*':
            result = num1 * num2;
            printf("Resultado: %.2f\n", result);
            break;
        case '/':
            if (num2 == 0) {
                printf("Erro: divisão por zero!\n");
            } else {
                result = num1 / num2;
                printf("Resultado: %.2f\n", result);
            }
            break;
        default:
            printf("Erro: operação inválida!\n");
    }

    return 0;
}
