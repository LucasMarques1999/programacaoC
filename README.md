#include <stdio.h>

typedef struct {
    char estado;
    char codigo[4];
    char nomeCidade[50];
    int populacao;
    float area;
    float pib;
    int pontoTuristico;
} carta;

int main() {
    carta cartas[2];

    for (int i = 0; i < 2; i++) {
        printf("\n--- Cadastro da Carta %d ---\n", i + 1);

        printf("Estado (A-H): ");
        scanf(" %c", &cartas[i].estado);

        printf("Código da Carta (ex: A01): ");
        scanf(" %s", cartas[i].codigo);

        printf("Nome da Cidade: ");
        scanf(" %s", cartas[i].nomeCidade);

        printf("População: ");
        scanf(" %d", &cartas[i].populacao);

        printf("Área (Km²): ");
        scanf(" %f", &cartas[i].area);

        printf("PIB (em bilhões de reais): ");
        scanf(" %f", &cartas[i].pib);

        printf("Número de Pontos Turísticos: ");
        scanf(" %d", &cartas[i].pontoTuristico);
    }

    for (int i = 0; i < 2; i++) {
        printf("\n\n--- Carta %d ---\n", i + 1);
        printf("Estado: %c\n", cartas[i].estado);
        printf("Código: %s\n", cartas[i].codigo);
        printf("Nome da Cidade: %s\n", cartas[i].nomeCidade);
        printf("População: %d\n", cartas[i].populacao);
        printf("Área: %.2f km²\n", cartas[i].area);
        printf("PIB: %.2f bilhões de reais\n", cartas[i].pib);
        printf("Número de Pontos Turísticos: %d\n", cartas[i].pontoTuristico);
    }

    return 0;
}






