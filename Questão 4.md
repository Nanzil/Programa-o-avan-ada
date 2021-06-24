#include<stdio.h>

int main()
{
    int valor,*p1;
    float temp, *p2;
    char aux, *nome =  "Ponteiros", *p3;
    int idade;
    int vetor[3], *p4, *p5;

    /* (a) */
    valor = 10;
    p1 = &valor;
    *p1 = 20;
    printf("%d \n", valor);
    // Como *p1, está recebendo o valor 20, ele está alocando na variavel valor e por isso o resultado deve sair 20. 
     /* (b) */
    temp = 26.5;
    p2 = &temp;
    *p2 = 29.0;
    printf("%.1f \n", temp); 
    // Semelhante ao resultado anterior devido o valor está sendo atribuido a um ponteiro, como já tem uma variavel atribuida a ele, ele alterar o valor da variavel 
    /* (c) */
    p3 = &nome[0];
    aux = *p3;
    printf("%c \n", aux);
    // A váriavel p3 está recebendo a letra "P" nesta operação e por ponteiro está passando para a variavel aux, o esperado é a letra P ser impressa.
     /* (d) */
    p3 = &nome[4];
    aux = *p3;
    printf("%c \n", aux);
    //A váriavel p3 está recebendo a letra "e" nesta operação e por ponteiro está passando para a variavel aux, o esperado é a letra e ser impressa.
     /* (e) */
    p3 = nome;
    printf("%c \n", *p3);
    // Como a variavel não foi passada por referencia e posição do vetor como na questão anterior p3 que é um ponteiro está indo na primeira posição do vetor para imprimi
    /* (f) */
    p3 = p3 + 4;
    printf("%c \n", *p3);
    // Como p recebeu a variavel nome na questão anterior, quando somado com 4 ele mostra o valor guardado no vetor nome na posição 4
    /* (g) */
    p3--;
    printf("%c \n", *p3);
    // Conforme o que já foi explicado na questão anterior, dessa vez foi subtraido 1 da posição do vetor que p3 está orientado.
    /* (h) */
    vetor[0] = 31;
    vetor[1] = 45;
    vetor[2] = 27;
    p4 = vetor;
    idade = *p4;
    printf("%d \n", idade);
     /* (i) */
    p5 = p4 + 1;
    idade = *p5;
    printf("%d \n", idade);
    /* (j) */
    p4 = p5 + 1;
    idade = *p4;
    printf("%d \n", idade);
    
    /* (l) */
    p4 = p4 - 2;
    idade = *p4;
    printf("%d \n", idade);
    // as questões h, i, j e l podem ser respondida com uma unica resposta. p4 está recebendo informação do vetor, mas cada posição do vetor tem uma infoção armazenada diferente e por isso que ao somar ou subtrair a posição do vetor o valor altera, após isso o valor é realocado pra posição  do vetor e quando manda imprimir a variavel idade ele imprimi a primeira posição.
    /* (m) */
    p5 = &vetor[2] - 1;   
    printf("%d \n", *p5);
    // o Veto
    /* (n) */
    p5++;
    printf("%d \n", *p5);
     
    return 0;
}
