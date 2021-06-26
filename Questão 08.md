#include<stdio.h>
int main(){
  int vet[] = {4,9,13};
  int i;
  for(i=0;i<3;i++){
  printf("%d ",*(vet+i));
  }
    return 0;
}
// Esse primeiro programa Imprimi em ordem crescente o valor de cada elemento armazenado no vetor vet com um espaço entre os numeros.
#include<stdio.h>
int main(){
  int vet[] = {4,9,13};
  int i;
  for(i=0;i<3;i++){
  printf("%X ",vet+i);
  }
    return 0;
}
// Esse segundo programa imprimi o endereço de memoria em que cada valor é armazenado inicialmente.
