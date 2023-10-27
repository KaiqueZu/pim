#include <stdio.h>
#include <string.h>

// Definindo uma estrutura para representar uma obra no museu
struct ObraMuseu {
    char titulo[100];
    char artista[100];
    float avaliacao;
};

int main() {
    int numObras;
    printf("Quantas obras deseja avaliar no museu? ");
    scanf("%d", &numObras);

    // Declarando um array de estruturas para armazenar as obras
    struct ObraMuseu obras[numObras];

    // Preenchendo informações sobre as obras
    for (int i = 0; i < numObras; i++) {
        printf("Obra #%d:\n", i + 1);
        printf("Título: ");
        scanf(" %[^\n]s", obras[i].titulo); // Lê o título incluindo espaços em branco
        printf("Artista: ");
        scanf(" %[^\n]s", obras[i].artista); // Lê o nome do artista incluindo espaços em branco
        obras[i].avaliacao = 0.0; // Inicializa a avaliação como 0
    }

    // Exibindo informações e permitindo avaliações
    int escolha;
    do {
        printf("\nEscolha uma obra para avaliar (1 a %d), 0 para sair: ", numObras);
        scanf("%d", &escolha);

        if (escolha >= 1 && escolha <= numObras) {
            printf("Avalie a obra '%s' de %s (0.0 a 10.0): ", obras[escolha - 1].titulo, obras[escolha - 1].artista);
            scanf("%f", &obras[escolha - 1].avaliacao);
        } else if (escolha != 0) {
            printf("Escolha inválida. Tente novamente.\n");
        }
    } while (escolha != 0);

    // Exibindo todas as avaliações das obras
    printf("\nAvaliações das Obras no Museu:\n");
    for (int i = 0; i < numObras; i++) {
        printf("Obra: %s\n", obras[i].titulo);
        printf("Artista: %s\n", obras[i].artista);
        printf("Avaliação: %.1f\n\n", obras[i].avaliacao);
    }

    return 0;
}
