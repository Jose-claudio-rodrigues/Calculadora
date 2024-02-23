# Calculadora
Calculadora com as 4 operações básicas 

#include <stdio.h>

int main() {
    float num1, num2, resultado;
    char operacao;

    printf("Digite a operacao que deseja realizar \n 1-soma \n 2-Subtracao \n 3-Multiplicacao \n 4-Divisao \n ");
    scanf("%c", &operacao);

    printf("Digite o primeiro numero: ");
    scanf("%f", &num1);

    printf("Digite o segundo numero: ");
    scanf("%f", &num2);

    switch(operacao) {
        case '1':
            resultado = num1 + num2;
            printf("Resultado: %.2f\n", resultado);
            break;
        case '2':
            resultado = num1 - num2;
            printf("Resultado: %.2f\n", resultado);
            break;
        case '3':
            resultado = num1 * num2;
            printf("Resultado: %.2f\n", resultado);
            break;
        case '4':
            if(num2 != 0) {
                resultado = num1 / num2;
                printf("Resultado: %.2f\n", resultado);
            } else {
                printf("Erro! Divisao por zero nao permitida.\n");
            }
            break;
        default:
            printf("Operacao invalida!\n");
    }

    return 0;
}
