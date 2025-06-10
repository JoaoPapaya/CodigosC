# CodigosC

```
#include <stdio.h>
#include <stdlib.h>
#include <math.h>

void Soma(int n, int n2){
    printf("digite dois números separados por vírgula:\n");
    scanf("%d, %d", &n, &n2); 
    printf("A soma deles é %d", n + n2);
}
void LoopPar(int i, int n){
        for(i = 0; i < 10; i++){
        printf("digite um número:\n");
        scanf("%d", &n);
        if(n % 2 == 0){
            printf("%d é par\n", n);
        }
       else{
            printf("%d é impar\n", n);
        }
    }
}
void Fahrenheit(int n){
    printf("Enter Fahrenheit temperatura: ");
    scanf("%d", &n);
    printf("Celsius temperatura: %.2f\n", 5.0/9*(n-32));
}

void MediaSeis(int n, int n2, int n3, int n4, int n5, int n6){
    printf("digite seis números separados por vírgula:\n");
    scanf("%d, %d, %d, %d, %d, %d", &n, &n2, &n3, &n4, &n5, &n6);
    printf("A média é: %.2f", (n + n2+ n3 + n4 + n5 + n6)/6);
}

void MediaPond(int n, int n2, int n3, int n4, int n5, int n6, float f){
    printf("digite três notas separadas por vírgula:\n");
    scanf("%d, %d, %d", &n, &n2, &n3);
    printf("%d, %d, %d", n, n2, n3);
    printf("Digite o peso de cada nota respectivamente:\n");
    scanf("%d, %d, %d", &n4, &n5, &n6);
    printf("%d, %d, %d", n4, n5, n6);
    f = ((n * n4) + (n2 * n5) + (n3 * n6))/(n4 + n5 + n6);
    printf("A média é: %.2f", f);    
}

void Inflacao(int n){
    printf("Digite o Valor do Produto:\n");
    scanf("%d", &n);

    if(n >= 100){
        n *= 1.2;
        printf("Seu Produto Inflacionou 20%, seu valor é : %d", n);
    } 
    else {
        n *= 1.1;
        printf("Seu Produto Inflacionou 10%, seu valor é: %d", n);
    }
}

void AnoBissexto(int n){
    printf("digite um ano:\n");
    scanf("%d", &n);
   
    if((n%4 == 0) && ((n%100 != 0) || (n%400 == 0))){
        printf("o ano é bissexto");
    }
    else{
        printf("o ano não é bissexto");
    }
}

void RaizDeN(int n){
    printf("digite um número:\n");
    scanf("%d", &n);
    printf("A raiz quadrada desse número é: %d", sqrt(n));
}

void TipoTriangulo(int n, int n2, int n3){
    printf("digite a medida de cada lado do triângulo separados por vírgula:\n");
    scanf("%d, %d, %d", &n, &n2, &n3);
    if(n == n2 && n2 == n3){
        printf("O triangulo é equilátero");
    }
    else if((n == n2 || n == n3) ^ n2 == n3){
        printf("O triângulo é isósceles");
    }
    else{
        printf("O triângulo é escaleno");
    }
}

void RaizDeDois(int n, int i){
    printf("digite um número natural:\n");
    scanf("%d", &n);
    while(exp2(i) < n){
        i++;
    }
    if(exp2(i) == n){
        printf("O número é potência de dois");
    }
    else{
        printf("O número não é potência de dois");
    }
}

void ParOuImpar(int n){
    printf("digite um número:\n");
    scanf("%d", &n);
    if(n%2 == 0){
        printf("o nº é par");
    }
    else{
        printf("o nº é impar");
    }
}

void MaiorNumero(int n, int n2, int n3){
    printf("digite três números separados por vírgula:\n");
    scanf("%d, %d, %d", &n, &n2, &n3);
    if(n > n2 && n > n3){
        printf("%d é o maior número", n);
    }
    else if(n2 > n && n2 > n3){
        printf("%d é o maior número", n2);
    }
    else if(n3 > n2 && n3 > n){
        printf("%d é o maior número", n3);
    }
    else{
        printf("Os números são iguais");
    }
}

void Pagamento(float v, int o, int p){
    printf("Digite o valor gasto:\n");
    scanf("%f", &v);
    printf("Digite a forma de pagamento:\n1 - A vista\n2 - Duas Parcelas\n3 - Três parcelas\n");
    scanf("%d", &o);
  
    if(o == 1){
      v = v - (v/10);
    }
    if(o == 3 && v >= 100){
      printf("Digite a quantidade de parcelas, entre 3 e 10:\n");
      scanf("%d", &p);
      if(p >= 3 && p <= 10){
        v = v/p;
        v = (v + (v * 0.03)) * p;
      }
    }

  printf("O valor a ser pago é %.2f", v);
}

int main() {
    int n, n2, n3, n4, n5, n6, i, opcao, parcela;
    float valor, f, f2, f3;
    
        return 0;
}
```

## Código questão 34

```
#include <stdio.h>
int main() {

    char nome[100];
    char endereco[100];
    int n, n2;

printf("Digite seu nome\n");
    scanf("%[^\n]%*c", &nome);
  
    printf("Digite seu endereço\n");
    scanf("%[^\n]%*c", &endereco);
  
    printf("Digite seu telefone\n");
    scanf("%d", &n);
  
    printf("Digite sua idade\n");
    scanf("%d", &n2);

    printf("seu nome é %s, seu endereço é %s, seu telefone é %d, sua idade é %d", nome, endereco, n, n2);
    
        return 0;
}
```
## Questão 44
```
// Online C compiler to run C program online
#include <stdio.h>

void maior (float principal, float f2, float f3){
    if((principal > f2) && (principal > f3)){
        printf("%.2f é o maior\n", principal);
    }
}
void menor (float principal, float f2, float f3){
    if((principal < f2) && (principal < f3)){
        printf("%2.f é o menor\n", principal);
    }
}
void meio (float principal, float f2, float f3){
    if((principal < f2) && (principal > f3) || (principal > f2) && (principal < f3)){
        printf("%.2f é o do meio\n", principal);
    }
}

int main() {
    
    float f, f2, f3;
    
    printf("digite o 1º valor: ");
    scanf("%f", &f);
    printf("digite o 2º valor: ");
    scanf("%f", &f2);
    printf("digite o 3º valor: ");
    scanf("%f", &f3);
    
    maior(f, f2, f3);
    maior(f2, f, f3);
    maior(f3, f2, f);    
    meio(f, f2, f3);    
    meio(f2, f, f3);    
    meio(f3, f2, f);    
    menor(f, f2, f3);
    menor(f2, f, f3);
    menor(f3, f2, f);    
    
    return 0;
}
```
