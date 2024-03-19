#include <stdio.h>
#include <stdbool.h>
5)
// Função para verificar se um número é primo
bool primo(int numero) {
    // Se o número for menor ou igual a 1, não é primo
    if (numero <= 1)
        return false;
    
    
    for (int i = 2; i * i <= numero; i++) {
        if (numero % i == 0)
            return false; 
    }
    return true; // Se não for divisível por nenhum número, é primo
}

int main() {
    int num;
    printf("Digite um número inteiro: ");
    scanf("%d", &num);

    if (primo(num))
        printf("%d é um número primo\n", num);
    else
        printf("%d não é um número primo\n", num);
    
    return 0;
}

6) #include <stdio.h>

double calcular_valor_serie(int n) {
    double soma = 0.0; 
    
  int sinal = 1; 

    for (int k = 1; k <= n; ++k) {
        soma += sinal * (double)k / (k * k); 
        sinal *= -1; 
    }

    return soma; 
}

int main() {
    int n;

    
    printf("Digite um valor numerico inteiro: ");
    scanf("%d", &n);

   
    double resultado = calcular_valor_serie(n);

    
    printf("O resultado da expressao e aproximadamente: %.10f\n", resultado);

    return 0; 
}
