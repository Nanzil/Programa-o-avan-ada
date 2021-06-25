#include<stdio.h>
int main(){
    int pulo[5];
    pulo[2]=7;
    printf("%d ",*(pulo + 2));
    //O uníco que mostra o valor armazenado no terceiro elemento é essa expressão 
    printf("%d ",*(pulo + 4));
    printf("%d ",pulo + 2);
    printf("%d ",pulo + 4);
    return 0;
}
