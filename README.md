# Jogo-chatgpt
# Desafio modulo 2 da DIO - DEsenvolver um jogo simples em linguagem C com ajuda do Chatgpt
# Jogo adivinhe o número

//Esse jogo gera um número aleatório entre 1 e 100 e permite que o jogador tente adivinhar, dando dicas se o palpite está alto ou baixo.

#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int numero_secreto, palpite, tentativas = 0;
    srand(time(NULL)); // Inicializa a semente do gerador de números aleatórios
    numero_secreto = rand() % 100 + 1; // Número entre 1 e 100
    
    printf("Bem-vindo ao jogo Adivinhe o Número!\n");
    printf("Tente adivinhar um número entre 1 e 100.\n");
    
    do {
        printf("Digite seu palpite: ");
        scanf("%d", &palpite);
        tentativas++;
        
        if (palpite > numero_secreto) {
            printf("Muito alto! Tente novamente.\n");
        } else if (palpite < numero_secreto) {
            printf("Muito baixo! Tente novamente.\n");
        } else {
            printf("Parabéns! Você acertou em %d tentativas.\n", tentativas);
        }
    } while (palpite != numero_secreto);
    
    return 0;
}

//Esse jogo gera um número aleatório entre 1 e 100 e permite que o jogador tente adivinhar, dando dicas se o palpite está alto ou baixo.


