#include<stdio.h>
int main(){
    int *p, mat[5], x;
    p = mat + 1;
    p = mat++;
    // não é valido 
    p = ++mat;
    // não é valido
    x = (*mat)++;
    printf("%d ",p);
    printf(x);
    return 0;
}
