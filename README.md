#include <stdio.h>
#include <stdlib.h>

void menu();
void somar();
void subtrair();
void multiplicar();
void dividir();

int main() {
    int opcao;

    do {
        menu();
        printf("\nEscolha uma opcao: ");
        scanf("%d", &opcao);

        switch(opcao) {
            case 1:
                somar();
                break;
            case 2:
                subtrair();
                break;
            case 3:
                multiplicar();
                break;
            case 4:
                dividir();
                break;
            case 0:
                printf("Saindo da calculadora...\n");
                break;
            default:
                printf("Opcao invalida. Tente novamente.\n");
        }

        system("pause"); // Pausa para visualizar o resultado
        system("cls");   // Limpa a tela (Windows)

    } while(opcao != 0);

    return 0;
}

void menu() {
    printf("====== CALCULADORA EM C ======\n");
    printf("1. Somar\n");
    printf("2. Subtrair\n");
    printf("3. Multiplicar\n");
    printf("4. Dividir\n");
    printf("0. Sair\n");
    printf("==============================\n");
}

void somar() {
    float a, b;
    printf("Digite o primeiro numero: ");
    scanf("%f", &a);
    printf("Digite o segundo numero: ");
    scanf("%f", &b);
    printf("Resultado: %.2f + %.2f = %.2f\n", a, b, a + b);
}

void subtrair() {
    float a, b;
    printf("Digite o primeiro numero: ");
    scanf("%f", &a);
    printf("Digite o segundo numero: ");
    scanf("%f", &b);
    printf("Resultado: %.2f - %.2f = %.2f\n", a, b, a - b);
}

void multiplicar() {
    float a, b;
    printf("Digite o primeiro numero: ");
    scanf("%f", &a);
    printf("Digite o segundo numero: ");
    scanf("%f", &b);
    printf("Resultado: %.2f * %.2f = %.2f\n", a, b, a * b);
}

void dividir() {
    float a, b;
    printf("Digite o primeiro numero: ");
    scanf("%f", &a);
    printf("Digite o segundo numero: ");
    scanf("%f", &b);
    if(b == 0) {
        printf("Erro: divisao por zero nao e permitida!\n");
    } else {
        printf("Resultado: %.2f / %.2f = %.2f\n", a, b, a / b);
    }
}
