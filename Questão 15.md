#include<stdio.h>
#include<stdlib.h>
#include<time.h>
void crescente(int tam, float *vet){
     float aux;
    for (int i = 0; i < tam; i++)
    {
        for (int j = 0; j < tam; j++)
        {
            if(vet[i] < vet[j]){
                aux = vet[i];
                vet[i] = vet[j];
                vet[j] = aux;
            }
        }
    }
}


int main() {
    
    int tam;
    printf("Digite a quantidade de valores que deseja armazenar:");
  
    scanf("%d", &tam); 
    float *vet;
    vet = (float*)(malloc(tam * sizeof(float)));
    for(int i = 0; i < tam; i++){
        printf("Digite o %d numero que deseja adicionar:  ", i+1);
        scanf("%f", &vet[i]);
}
    
    
    crescente (tam, vet);
    
    
    
      for (int i = 0; i < tam; i++)
    {
        printf("%.2f ", vet[i]);
    }
    free(vet);


return 0;
}
