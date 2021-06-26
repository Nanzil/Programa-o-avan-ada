#include<stdio.h>
int main(void){
  float vet[5] = {1.1,2.2,3.3,4.4,5.5};
  float *f;
  int i;
  f = vet;
  printf("contador/valor/valor/endereco/endereco");
  for(i = 0 ; i <= 4 ; i++){
    printf("\ni = %d ",i);
    printf("vet[%d] = %.1f ",i, vet[i]);
    printf("*(f + %d) = %.1f ",i, *(f+i));
    printf("&vet[%d] = %X ",i, &vet[i]);
    printf("%d \n", "(f + %d) = %X ",i, f+i);
  }
// Os valores estão aparecendo iguais tanto para o vetor quanto para o o ponteiro, o que era de se esperar, pois se alterar em um deve também alterar no outro. E por fim está sendo impresso o endereço de memoria armazanada a cada plotagem
    return 0;
}
