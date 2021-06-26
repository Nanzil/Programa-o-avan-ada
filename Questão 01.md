#include<stdio.h>
int main(void){
    int i=3,j=5;
    int *p = &i,*q = &j;
    if (p == &i)
    {
      printf("Resultado: Verdadeiro(%d)\n\n", p == &i  ); 
      // O valor informado é o esperado, devido o p "localizar", o local armazenado que é  a variavel i
    }else{
        printf("Resultado: Falso(%d)\n\n", p == &i );
    }
    printf("*p - *q = %d \n\n",*p - *q );
    //O resultado esperado realmente ´-2, pois os os valores referente a posição que os ponteiros p e q apontam são respctivamente 3 e 5
    printf("**&p = %d \n\n", **&p );
    // Essa expressão mostra exatamente o valor que p representa e o esperado realmente é 3
    printf("3 - *p/(*q) + 7 = %d \n\n", 3 - *p/(*q) + 7 );
    //O valor dessa expressão tem que ser 10, devido siginificar 3 -3/5 +7=10
    return 0;
}
