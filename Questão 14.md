#include<stdio.h>
#include<stdlib.h>
#include<time.h>

// A função comp foi criada para realizar a comparação entre cada valor armazenado no vetor
int comp(const void *a, const void *b){
    if (*(int*)a > *(int*)b) {
      return 1;
      // retorna 1 caso a seja maior que b
   } else if (*(int*)a < *(int*)b) {
      return -1;
      //-1 caso a seja menor
   } else {
      return 0;
      ////e retorna 0 caso não seja nenhum dos resultados anteriores
   }
}
// Esses valores são a informção que a função qsort() utiliza para ordenar o vetor. Caso for necessário ordenar o vetor de maneira descrecente é só alterar o sinal de 1 e -1 dessa função comp

int main() {
    
    int tam; // Criado a variavel do tamanho do vetor
    printf("Digite a quantidade de valores que deseja armazenar:");
    // solicitado ao usuario a o tamanho do vetor
    scanf("%d", &tam); // O usuário inseri o tamanho do vetor
    
    float *vet;// criado o vetor 
    vet = (float*)(malloc(tam * sizeof(float)));// Armazenado o vetor com alocação de memiria 
    for(int i = 0; i < tam; i++){
        printf("Digite o %d numero que deseja adicionar:  ", i+1);
        scanf("%f", &vet[i]);
        // preenchido o vetor pelo o usuário
}
    qsort(vet, tam, sizeof(float),comp);// organizado o vetor em ordem crescente pela função qsort
      for (int i = 0; i < tam; i++)
    {
        printf("%.2f ", vet[i]);
        // Impresso na tela o vetor ordenado de forma crescente 
    }
    free(vet);// Liberado o espaço de memoria que estava sendo usado pela alocação de memoria 
     
    
return 0;
}
