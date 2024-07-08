#include <stdio.h>
#include <stdlib.h>
#include <math.h>

int main()
{
    float raio, area;

    const float PI = 3.14;

    printf("Digite o raio: ");
    scanf("%f", &raio);

    area = PI * pow(raio, 2);

    printf("Area da circunferencia: %.2f", area);
}
