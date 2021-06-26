#include<stdio.h>

int main(void){
    char y[4];
    for(int i = 0; i < 4; i++){
    printf(" y + %d = %X \n", i , y + i );
    }
    int x[4];
    for(int i = 0; i < 4; i++){
    printf(" x + %d = %X \n", i , x + i);
    }
    float z[4];
    for(int i = 0; i < 4; i++){
        printf(" z + %d = %X \n", i , z + i);
    }
     double h[4];

    for(int i = 0; i < 4; i++){
        printf(" h + %d = %X \n", i , h + i);
    }
    return 0;
}

// O resultado obtido foi semelhante ao esperado, em relação ao tamanho de cada variavél, porém foi mostrado o endereço de memoria armazenado cada váriavel 
