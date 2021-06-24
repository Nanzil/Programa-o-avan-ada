#include<stdio.h>
int main(void){
   int i=5,j=3, *p, *q;
    p = &i;
    q = &j;
    p = i;
    // É ilegal, pois o valor alocado em i será o mesmo mostrando quando imprimir p, porém p não pode receber i, pois é um ponteiro e i é um valor de referencia 
    q = &j;
    p = &*&i;
    i = (*&)j; 
    // ilegal pois o & não está referenciando nada;
    i = *&j;
    i = *&*&j;
    q = *p;
    // É ilegal pois p não tem valor de referencia alocado nele, pois q é um ponteiro tem que receber um valor por referencia
    i = (*p)++ + *q;
    return 0;
}


