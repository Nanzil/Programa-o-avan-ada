
#include <stdio.h>
int multiplicacao(int a, int b){
    return a*b;
}
int main() {
  int i, j, c;
  int (*p) (int, int);
  printf("Insira o primeiro valor da multiplicação ");
  scanf("%d", &i);
  printf("Insira o segundo valor da multiplicação ");
  scanf("%d", &j);
  p = multiplicacao;
  c= p(i,j);
  printf("O resultado é: ");
  printf("%d", c,"\n");
  printf("Insira o primeiro valor da multiplicação ");
  scanf("%d", &i);
  printf("Insira o segundo valor da multiplicação ");
  scanf("%d", &j);
  p = multiplicacao;
  c= p(i,j);
  printf("O resultado é: ");
  printf("%d", c);
    return 0;
}
// A função criada nesse programa foi para multiplicação de dois valores. P é o ponteiro que é atribuida a função multplicacao que realiza a multiplicação entre as duas váriaveis. Assim, a qualquer momento que for chamado o ponteiro e inserido uma nova váriavel ocorre a multiplicação.
