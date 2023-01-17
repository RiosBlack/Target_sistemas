## Pergunta 1:
Observe o trecho de código abaixo:
int INDICE = 13, SOMA = 0, K = 0;
enquanto K < INDICE faça
{
K = K + 1;
SOMA = SOMA + K;
}
imprimir(SOMA);
Ao final do processamento, qual será o valor da variável SOMA?


## Resposta:

O valor da variável soma é 91 conforme resolução abaixo:

* Código em Java:

public class Main {
    public static void main(String[] args) {

        int indice = 13;
        int soma  = 0;
        int k = 0;

        for (int i = 0; i < indice; i++) {
            k = k + 1;
            soma = soma + k;
            System.out.println("A quantidade da interação é " + i + " | " + " O valor do indice é " + indice + " | " +  " O valor de K é " + k +  " | " +  " O valor de soma é " + soma);
        }
        System.out.println("O valor da variavel soma é " + soma);
        System.out.println("Fim");
    }

}

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Pergunta 2: 

2) Dado a sequência de Fibonacci, onde se inicia por 0 e 1 e o próximo valor sempre será a soma dos 2 valores anteriores (exemplo: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34...), escreva um programa na linguagem que desejar onde, informado um número, ele calcule a sequência de Fibonacci e retorne uma mensagem avisando se o número informado pertence ou não a sequência.

IMPORTANTE:
Esse número pode ser informado através de qualquer entrada de sua preferência ou pode ser previamente definido no código;


## Resposta 2:

Fiz um código abaixo que resolve o problema:

* Código em Java:

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        int numero1 = 0;
        int numero2 = 1;
        int numero3 = 0;

        System.out.println("Iniciando consulta de sequência de fibonacci");
        Scanner scanner = new Scanner(System.in);
        System.out.println("Digite um valor para consulta");
        int numeroEscolhido = scanner.nextInt();

        while (numeroEscolhido > numero3){
            numero3 = numero1 + numero2;
            numero1 = numero2;
            numero2 = numero3;
        }

        if (numeroEscolhido == 0 || numeroEscolhido == 1 || numeroEscolhido == numero3) {
            System.out.println("O numero escolhido é da sequencia.");
        } else {
            System.out.println("O numero não está na sequecia.");
        }
        System.out.println("Fim");

    }

}
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
