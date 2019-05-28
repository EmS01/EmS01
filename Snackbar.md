#include <stdio.h>
#include <stdlib.h>

int main(void)
{
  int execucao;
  int i;  
 
 void Layout(void){
    printf("______________________________________\n");
    printf("  CODIGO   |  ESPECIFICACAO  | PRECO  \n");
    printf("--------------------------------------\n");
    printf("  1        | Cachorro Quente | R$ 4.00\n");
    printf("  2        |     X-Salada    | R$ 4.50\n");
    printf("  3        |     X-Bacon     | R$ 5.00\n");
    printf("  4        | Torrada Simples | R$ 2.00\n");
    printf("  5        |   Refrigerante  | R$ 1.50\n");
    printf("--------------------------------------\n\n");
 	
 }
/* criar vetor para ler mais de um produto */ 
 struct ficha_do_cliente
 {
   char nome[50];
   char cpf[30];
 };

struct ficha_do_funcionario{
  char nome[50];
  int codigof;
  float comissao;
};

 struct cadastro_pedido{
   int request;
   int codigo;
   int qtd;
   float preco;
   float comissao;
 };

 /* instancia uma estrutura e a nomeia */
 struct ficha_do_cliente cliente;      
 struct ficha_do_funcionario funcionario; 
 struct cadastro_pedido pedido;
 
 printf("**** BEM VINDO AO SYSTEM SNACKBAR ****\n\n\n\n\n");

 do{
    printf("____________ Informacao do Cliente ____________\n\n\n");

    printf("Nome do cliente: ");
    fflush(stdin);                        
    fgets(cliente.nome, 40, stdin);     
    printf("CPF: ");
    fflush(stdin);
    fgets(cliente.cpf, 40, stdin);

    printf("\n____________ Informacao do Funcionario ____________\n\n\n");

    printf("Nome do funcionario: ");
    fflush(stdin);
    fgets(funcionario.nome, 40, stdin);
    printf("Codigo do funcionario: ");
    scanf("%d", &funcionario.codigof);
    
    system("cls");

    printf("\n\n ____________ Informacoes Registradas  ____________\n\n");

    /* imprime os dados lidos*/
    printf("Nome do Cliente: %s", cliente.nome);
    printf("CPF: %s", cliente.cpf);
    printf("Funcionario: %s" , funcionario.nome);
    printf("Codigo do funcionario: %d\n", funcionario.codigof);
    printf("Pedidos do cliente: %d\n", pedido.codigo);
    printf("\n");

	Layout();
	
    printf("\n____________ Pedidos ____________\n\n\n");
    printf("Codigo do pedido: ");
    scanf("%d", &pedido.codigo);
    printf("\nDeseja cadastrar novo pedido?\n");
    printf(" 1 - sim      |    2 - nao  \n");
    scanf("%d", &pedido.request);
    system("cls");
  
    switch(pedido.codigo){
      case 1:
	      pedido.preco = 4;
	      printf("\nPedido selecionado: Cachorro Quente\n");
	      printf("Informe a quantidade:");
  	    scanf("%d", &pedido.qtd);
        system("cls");
	      pedido.preco = pedido.qtd*4;
	      printf("\nTotal a pagar..: R$  %.2f\n\n\n", pedido.preco);
        funcionario.comissao = pedido.preco*0.1;
        printf("\nComissao: %.2f\n", funcionario.comissao);
        printf("Funcionario: %s", funcionario.nome);
        printf("Codigo do funcionario: %d\n", funcionario.codigof);
	      break;

       case 2:
	      pedido.preco = 4.5;
	      printf("\nPedido selecionado: X-Salada\n");
	      printf("Informe a quantidade:");
  	    scanf("%d", &pedido.qtd);
        system("cls");
	      pedido.preco = pedido.qtd*4.5;
	      printf("\nTotal a pagar: R$  %.2f\n\n\n", pedido.preco);
        funcionario.comissao = pedido.preco*0.1;
        printf("\nComissao: %.2f\n", funcionario.comissao);
        printf("Funcionario: %s", funcionario.nome);
        printf("Codigo do funcionario: %d\n", funcionario.codigof);
	      break;

      case 3:
	      pedido.preco = 5;
	      printf("\nPedido selecionado:  X-Bacon\n");
	      printf("Informe a quantidade:");
  	    scanf("%d", &pedido.qtd);
        system("cls");
	      pedido.preco = pedido.qtd*5;
	      printf("\nTotal a pagar: R$  %.2f\n\n\n", pedido.preco);
        funcionario.comissao = pedido.preco*0.1;
        printf("\nComissao: %.2f\n", funcionario.comissao);
        printf("Funcionario: %s", funcionario.nome);
        printf("Codigo do funcionario: %d\n", funcionario.codigof);
	      break;
      case 4:
	      pedido.preco = 2;
	      printf("\nPedido selecionado: Torrada Simples\n");
	      printf("Informe a quantidade:");
  	    scanf("%d", &pedido.qtd);
        system("cls");
	      pedido.preco = pedido.qtd*2;
	      printf("\nTotal a pagar: R$  %.2f\n\n\n", pedido.preco);
        funcionario.comissao = pedido.preco*0.1;
        printf("\nComissao: %.2f\n", funcionario.comissao);
        printf("Funcionario: %s", funcionario.nome);
        printf("Codigo do funcionario: %d\n", funcionario.codigof);
	      break;
      case 5:
	      pedido.preco = 1.5;
	      printf("\nPedido selecionado: Refrigerante\n");
	      printf("Informe a quantidade:");
  	    scanf("%d", &pedido.qtd);
        system("cls");
	      pedido.preco = pedido.qtd*1.5;
	      printf("\nTotal a pagar: R$  %.2f\n\n\n", pedido.preco);
        funcionario.comissao = pedido.preco*0.1;
        printf("\nComissao: %.2f\n", funcionario.comissao);
        printf("Funcionario: %s", funcionario.nome);
        printf("Codigo do funcionario: %d\n", funcionario.codigof);
	      break;
       default:
	      printf("\nOperacao incorreta, tente novamente!!!\n");	
}
 printf("\n\nFECHAR?\n");
 printf("\n1 - sim   |   2- nao\n");
 scanf("%d", &execucao);
}while(execucao == 2);
 return(0);
}
