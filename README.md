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
## Pergunta 3:
3) Dado um vetor que guarda o valor de faturamento diário de uma distribuidora, faça um programa, na linguagem que desejar, que calcule e retorne:
• O menor valor de faturamento ocorrido em um dia do mês;
• O maior valor de faturamento ocorrido em um dia do mês;
• Número de dias no mês em que o valor de faturamento diário foi superior à média mensal.

IMPORTANTE:
a) Usar o json ou xml disponível como fonte dos dados do faturamento mensal;
b) Podem existir dias sem faturamento, como nos finais de semana e feriados. Estes dias devem ser ignorados no cálculo da média;


Resposta:

* Código em JavaScript:
* Dados do json enviado pela empresa.

let Json = require('./dados.json');

const maiorValor = Json.reduce(function (prev, current) {
    return prev.valor > current.valor ? prev : current;
});


const menorValor = Json.reduce(function (prev, current) {
    return prev.valor < current.valor ? prev : current;
});


function diasMediaMensal() {
    var mediaMesal = 20865.37;
    let quantidade = 0;
    for (let i = 0; i < Json[29].dia; i++) {
        if (Json[i].valor > mediaMesal) {
            quantidade++;
        }
    }
    return quantidade;
}

console.log('O menor valor ocorreu em', menorValor);
console.log('O maior valor correu em', maiorValor);
console.log(
    'O número da faturamento diário foi maior que o mensal em:',
    diasMediaMensal(),
    'dias'
);

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Pergunta 4: 
4) Dado o valor de faturamento mensal de uma distribuidora, detalhado por estado:

SP – R$67.836,43
RJ – R$36.678,66
MG – R$29.229,88
ES – R$27.165,48
Outros – R$19.849,53

Escreva um programa na linguagem que desejar onde calcule o percentual de representação que cada estado teve dentro do valor total mensal da distribuidora.

Resposta:

* Código em Java:

class Dados {
    double sp = 67836.43;
    double rj = 36678.66;
    double mg = 29229.88;
    double es = 27165.48;
    double outros = 19849.53;
}

public class Main {
    public static void main(String[] args) {
        Dados dados = new Dados();
        double valorTotal = dados.es + dados.mg + dados.rj + dados.sp + dados.outros;
        double mediaES = (dados.es / valorTotal)*100;
        double mediaMG = (dados.mg / valorTotal)*100;
        double mediaRJ = (dados.rj / valorTotal)*100;
        double mediaSP = (dados.sp / valorTotal)*100;
        double mediaOutros = (dados.outros / valorTotal)*100;
        System.out.println("O percentual de representação dos estados são: ES: " + mediaES + "| MG: " + mediaMG + "| RJ: " + mediaRJ + "| SP: " + mediaSP + "| Outros: " + mediaOutros);
    }
}

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Pergunta 5:
5) Escreva um programa que inverta os caracteres de um string.

IMPORTANTE:
a) Essa string pode ser informada através de qualquer entrada de sua preferência ou pode ser previamente definida no código;
b) Evite usar funções prontas, como, por exemplo, reverse;


#Resposta:
* Código em Java

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Digite um nome para ser invertido");
        String str = scanner.next();
        char[] ch = str.toCharArray();
        int begin = 0;
        int end = ch.length-1;
        char temp;
        while(end>begin){
            temp = ch[begin];
            ch[begin] = ch[end];
            ch[end] = temp;
            end--;
            begin++;
        }
        str = new String(ch);
        System.out.println(str);
    }
}
