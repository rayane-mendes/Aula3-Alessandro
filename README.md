1) Vetor de 10 posições preenchido com valores digitados pelo usuário (com for-each apenas na exibição)

import java.util.Scanner;

public class Exemplo1 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int[] vetor = new int[10];
       
        for (int i = 0; i < vetor.length; i++) {
            System.out.print("Digite o valor para a posição " + i + ": ");
            vetor[i] = scanner.nextInt();
        }
        
        System.out.println("Valores do vetor:");
        for (int valor : vetor) {
            System.out.print(valor + " ");
        }
        
        scanner.close();
    }
}

2) Matriz char que imprime o nome completo

Aqui está a matriz char com seu nome completo, usando for-each para exibir os valores.

public class Exemplo2 {
    public static void main(String[] args) {
        char[][] nome = {
            {'R', 'a', 'y', 'a'},
            {'n', 'e', ' ', 'M'},
            {'e', 'n', 'd', 'e'},
            {'s', ' ', 'A', 'l'},
            {'c', 'a', 'n', 't'},
            {'a', 'r', 'a', ' '}
        };

        for (char[] linha : nome) {
            for (char c : linha) {
                System.out.print(c);
            }
            System.out.println();
        }
    }
}

3) Matriz 5x5 com maior elemento (for-each na busca pelo maior valor)

import java.util.Scanner;

public class Exemplo3 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int[][] matriz = new int[5][5];
        
        for (int i = 0; i < matriz.length; i++) {
            for (int j = 0; j < matriz[i].length; j++) {
                System.out.print("Digite o valor para [" + i + "][" + j + "]: ");
                matriz[i][j] = scanner.nextInt();
            }
        }
        
        int maior = matriz[0][0];
        for (int[] linha : matriz) {
            for (int valor : linha) {
                if (valor > maior) {
                    maior = valor;
                }
            }
        }

        System.out.println("O maior valor da matriz é: " + maior);
        
        scanner.close();
    }
}

4) Programa para procurar um valor em um vetor de 10 elementos (com for-each apenas na exibição, pois a busca exige índice)

import java.util.Scanner;

public class Exemplo4 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int[] vetor = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};  // Vetor de exemplo
        boolean encontrado = false;
        
        System.out.print("Digite o valor que deseja procurar no vetor: ");
        int valor = scanner.nextInt();
  
        for (int i = 0; i < vetor.length; i++) {
            if (vetor[i] == valor) {
                System.out.println("O valor " + valor + " está na posição " + i + " do vetor.");
                encontrado = true;
                break;
            }
        }
  
        if (!encontrado) {
            System.out.println("O valor " + valor + " não existe no vetor.");
        }
        
        scanner.close();
    }
}

5) Programa para somar os elementos de cada linha de uma matriz 3x3 

import java.util.Scanner;

public class Exemplo5 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double[][] matriz = new double[3][3];
        
        
        for (int i = 0; i < matriz.length; i++) {
            for (int j = 0; j < matriz[i].length; j++) {
                System.out.print("Digite o valor para [" + i + "][" + j + "]: ");
                matriz[i][j] = scanner.nextDouble();
            }
        }
        
        
        int linhaNum = 0;
        for (double[] linha : matriz) {
            double soma = 0;
            for (double valor : linha) {
                soma += valor;
            }
            System.out.println("A soma dos elementos da linha " + linhaNum + " é: " + soma);
            linhaNum++;
        }
    }
}
