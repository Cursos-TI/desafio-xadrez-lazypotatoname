#include <stdio.h>

/* Função recursiva para movimentar a Torre (horizontal - Direita) */
void moverTorre(int casas_restantes) {
    if (casas_restantes <= 0) return;
    printf("Direita\n");
    moverTorre(casas_restantes - 1);
}

/* Função recursiva para movimentar a Rainha (horizontal - Esquerda) */
void moverRainha(int casas_restantes) {
    if (casas_restantes <= 0) return;
    printf("Esquerda\n");
    moverRainha(casas_restantes - 1);
}

/* Função recursiva para movimentar o Bispo (diagonal - Cima Direita) */
void moverBispoRecursivo(int casas_restantes) {
    if (casas_restantes <= 0) return;
    printf("Cima Direita\n");
    moverBispoRecursivo(casas_restantes - 1);
}

/* Movimento com loops aninhados para o Bispo (extra: exemplo didático com loops) */
void moverBispoComLoops(int casas) {
    printf("(Simulação do movimento do Bispo com loops aninhados)\n");
    for (int vertical = 0; vertical < casas; vertical++) {
        for (int horizontal = 0; horizontal < 1; horizontal++) {
            printf("Cima Direita\n");
        }
    }
}

/* Movimento complexo do Cavalo (2 cima, 1 direita) usando loops aninhados e controle de fluxo */
void moverCavaloComplexo(int movimentos) {
    int movimentos_feitos = 0;

    for (int i = 0; i < movimentos; i++) {
        for (int j = 0; j < 3; j++) {
            if (j < 2) {
                printf("Cima\n");
                continue; // Continua para a segunda casa para cima
            }
            if (j == 2) {
                printf("Direita\n");
                break; // Sai do loop interno após completar o "L"
            }
        }
        movimentos_feitos++;
    }
}

int main() {
    // ---------------- Torre ----------------
    printf("Movimento da Torre (5 casas para a Direita - recursivo):\n");
    moverTorre(5);

    printf("\n");

    // ---------------- Bispo ----------------
    printf("Movimento do Bispo (5 casas na Diagonal - Cima Direita - recursivo):\n");
    moverBispoRecursivo(5);

    printf("\n");

    // Loops aninhados extra do Bispo (vertical externo, horizontal interno)
    moverBispoComLoops(5);

    printf("\n");

    // ---------------- Rainha ----------------
    printf("Movimento da Rainha (8 casas para a Esquerda - recursivo):\n");
    moverRainha(8);

    printf("\n");

    // ---------------- Cavalo ----------------
    printf("Movimento do Cavalo (movimento em 'L' - 2 casas Cima, 1 Direita - com loops complexos):\n");
    moverCavaloComplexo(1); // Você pode aumentar para mais de um movimento em "L", se quiser

    return 0;
}
