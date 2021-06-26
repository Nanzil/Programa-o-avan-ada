#include<stdio.h>
int main(void){
   int i=5, *p;
    p = &i;
    printf("%x %d %d %d %d", p,*p+2,**&p,3**p,**&p+4);
    // Ao imprimir o p, o programa mostra um valor diferente a cada plotagem, devido o local de memoria dele vária já que ele aponta para uma variavel fixa que é i que está na posição 4094, e os valores seguintes estão corretos, pois as operação são realizadas com o valor alocado no i (os valores são :5, 7, 15 e 9.
    return 0;
}


