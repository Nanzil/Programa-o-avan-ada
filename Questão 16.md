//Programa 13
#include<stdio.h>
#include<stdlib.h>
#include<time.h>
int main() {
    clock_t tempo;
    int tam;
    printf("Digite a quantidade de valores que deseja armazenar:");
    scanf("%d", &tam);

    float *vet;
    vet = (float*)(malloc(tam * sizeof(float)));
    for(int i = 0; i < tam; i++){
        printf("Digite o %d numero que deseja adicionar:  ", i+1);
        scanf("%f", &vet[i]);
}
    tempo = clock();
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
      for (int i = 0; i < tam; i++)
    {
        printf("%.2f ", vet[i]);
    }
    free(vet);
    tempo= clock() - tempo;
    printf("\n segundos:   %f ", tempo);
return 0;
}



// Programa 14



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
    clock_t tempo;
    int tam;
    printf("Digite a quantidade de valores que deseja armazenar:");
    scanf("%d", &tam); 
    float *vet;
    vet = (float*)(malloc(tam * sizeof(float)));
    for(int i = 0; i < tam; i++){
        printf("Digite o %d numero que deseja adicionar:  ", i+1);
        scanf("%f", &vet[i]);
}
    tempo = clock();
    crescente (tam, vet);
    
      for (int i = 0; i < tam; i++)
    {
        printf("%.2f ", vet[i]);
    }
    free(vet);

    tempo= clock() - tempo;
    printf("\n segundos:   %f ", tempo);
return 0;
}




// Se comparado os dois códigos o código com a função qsort() foi mais rápido no momento da exucção do que no programa criado por mim, os dois foram analisados após a coleta dos dados, pois foi praticamente igual a coleta dos dois programas

















