#include <stdio.h>

int main() {
    int opcao;
    
    do {
        printf("=== Menu ===\n");
        printf("1. Questão A\n");
        printf("2. Questão B\n");
        printf("3. Questão C\n");
        printf("4. Sair\n");
        printf("Digite a opção desejada: ");
        scanf("%d", &opcao);
        
        switch (opcao) {
            case 1:
                // Questão A
                {
                    int i, numero, pares = 0;
                    printf("Digite 5 números inteiros:\n");
                    for (i = 0; i < 5; i++) {
                        scanf("%d", &numero);
                        if (numero % 2 == 0) {
                            printf("%d é par.\n", numero);
                            pares++;
                        }
                    }
                    printf("Foram digitados %d números pares.\n", pares);
                }
                break;
            case 2:
                // Questão B
                {
                    int i, numero, maior = 0, menor = 0;
                    printf("Digite 5 números inteiros:\n");
                    for (i = 0; i < 5; i++) {
                        scanf("%d", &numero);
                        if (i == 0 || numero > maior) {
                            maior = numero;
                        }
                        if (i == 0 || numero < menor) {
                            menor = numero;
                        }
                    }
                    printf("O maior número digitado foi %d e o menor foi %d.\n", maior, menor);
                }
                break;
            case 3:
                // Questão C
                {
                    int i, numero;
                    printf("Digite um número inteiro: ");
                    scanf("%d", &numero);
                    printf("Tabuada do %d:\n", numero);
                    for (i = 1; i <= 10; i++) {
                        printf("%d x %d = %d\n", numero, i, numero * i);
                    }
                }
                break;
            case 4:
                printf("Encerrando o programa...\n");
                break;
            default:
                printf("Opção inválida. Tente novamente.\n");
                break;
        }
        
        printf("\n");
    } while (opcao != 4);
    
    return 0;
}
