#include <stdio.h>
#include <string.h>

int main() {
    char nomes[3][50];
    int i, j;
    
    printf("Digite 3 nomes:\n");
    for (i = 0; i < 3; i++) {
        printf("Nome %d: ", i + 1);
        setbuf(stdin, NULL);
        gets(nomes[i]);
    }

    printf("\nMatriz de nomes:\n");
    for (int i = 0; i < 3; i++) {
        printf("Nome %d: %s\n", i+1, nomes[i]);
        printf("\n");
    }
}
