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
