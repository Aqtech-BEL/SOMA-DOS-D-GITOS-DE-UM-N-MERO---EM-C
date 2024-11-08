LINGUAGEM - C:
Código que pede para o usuário digitar um número inteiro positivo e o 
programa informa quanto é a soma dos dígitos desse número.

  
  
    #include <stdio.h>
    
    int main(){
      
      int num, resto = 0, soma = 0;
      
      //SOLICITA UM NÚMERO POSITIVO AO USUÁRIO
      printf("Veja a soma dos digitos de um número!\n");
     
      do{
          printf("Digite um número positivo: ");
          scanf("%d", &num);
          
          if(num < 0){
              printf("Digite um número positivo: ");
              scanf("%d", &num);
          }
      
      //IDENTIFICA SE O USUÁRIO ESTÁ DIGITANDO UM NÚMERO MENOR QUE ZERO
      }while(num < 0);
      
      
      //LAÇO DE REPETIÇÃO "WHILE" PARA SOMA DAS UNIDADES DO NÚMERO
      while(num > 0){
          
          resto = num % 10; //VARIÁVEL QUE RECEBE O RESTO DA DIVISÃO
          //printf("%d ", resto); //IMPRIME O RESTO
         
          num = num / 10; //VARIÁVEL RECEBE O QUOCIENTE (RESULTADO) DA DIVISÃO
          soma = soma + resto; //AQUI SE FAZ A SOMA DE CADA UNIDADE
          
      }
      
      /*LAÇO DE REPETIÇÃO "FOR" PARA SOMA DAS UNIDADES DO NÚMERO
      for(;num > 0; num = num /10){
          resto = num % 10;
          soma = soma + resto;
      }*/
      
      printf("\n A soma dos digitos é: %d", soma);
      
      
  
      return 0;
    }
