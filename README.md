#include <stdio.h>

int main() {
    // Movimento da Torre: 5 casas para a direita usando FOR
    printf("Movimento da Torre (5 casas para a Direita):\n");
    for (int i = 0; i < 5; i++) {
        printf("Direita\n");
    }

    printf("\n");

    // Movimento do Bispo: 5 casas na diagonal (Cima Direita) usando WHILE
    printf("Movimento do Bispo (5 casas na Diagonal - Cima Direita):\n");
    int contador_bispo = 0;
    while (contador_bispo < 5) {
        printf("Cima Direita\n");
        contador_bispo++;
    }

    printf("\n");

    // Movimento da Rainha: 8 casas para a esquerda usando DO-WHILE
    printf("Movimento da Rainha (8 casas para a Esquerda):\n");
    int contador_rainha = 0;
    do {
        printf("Esquerda\n");
        contador_rainha++;
    } while (contador_rainha < 8);

    printf("\n");

    // Movimento do Cavalo: 2 casas para baixo, depois 1 casa para a esquerda
    printf("Movimento do Cavalo (movimento em 'L' - 2 casas Baixo, 1 casa Esquerda):\n");

    // O loop externo será um FOR (obrigatório)
    for (int i = 0; i < 1; i++) {
        // Simula duas casas para baixo usando um WHILE
        int j = 0;
        while (j < 2) {
            printf("Baixo\n");
            j++;
        }

        // Depois das duas casas para baixo, move uma casa para a esquerda
        printf("Esquerda\n");
    }

    return 0;
}

