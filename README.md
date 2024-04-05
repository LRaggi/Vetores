# Vetores
# 1
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        int[] vetor = new int[10];
        Scanner input = new Scanner(System.in);
        System.out.println("Preencha com 10 números inteiros:");
        for (int i = 0; i < 10; i++) {
            vetor[i] = input.nextInt();
        }
        System.out.println("Números primos e suas respectivas posições:");
        for (int i = 0; i < 10; i++) {
            if (isPrime(vetor[i])) {
                System.out.println("Número Primo: " + vetor[i] + ", Posição: " + i);
            }
        }
    }
    public static boolean isPrime(int num) {
        if (num <= 1) {
            return false;
        }
        for (int i = 2; i <= num / 2; i++) {
            if (num % i == 0) {
                return false;
            }
        } return true;
    }
}
# 2
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        int[] vetor1 = new int[10];
        int[] vetor2 = new int[10];
        int[] vetorResultante = new int[20];
        Scanner input = new Scanner(System.in);
        System.out.println("Preencha o primeiro com 10 números:");
        for (int i = 0; i < 10; i++) {
            vetor1[i] = input.nextInt();
        } System.out.println("Preencha o segundo com 10 números:");
        for (int i = 0; i < 10; i++) {
            vetor2[i] = input.nextInt();
        } int j = 0;
        for (int i = 0; i < 10; i++) {
            vetorResultante[j++] = vetor1[i];
            vetorResultante[j++] = vetor2[i];
        } System.out.println("Resultado da Intercalação:");
        for (int i = 0; i < 20; i++) {
            System.out.print(vetorResultante[i] + " ");
        }
    }
}
# 3
import java.util.Random;
public class Main {
    public static void main(String[] args) {
        int[] vetor = new int[10];
        Random rand = new Random();
        double soma = 0;
        for (int i = 0; i < 10; i++) {
            vetor[i] = rand.nextInt(100); 
            soma += vetor[i];
        } double media = soma / 10;
        System.out.println("Vetor de 10 números aleatórios:");
        for (int i = 0; i < 10; i++) {
            System.out.print(vetor[i] + " ");
        } System.out.println("\nMédia: " + media);
    }
}
# 4
import java.util.Random;
public class Main {
    public static void main(String[] args) {
        int[] vetor = new int[20];
        Random rand = new Random();
        boolean found = false;
        for (int i = 0; i < 20; i++) {
            vetor[i] = rand.nextInt(30) + 1;
        } System.out.println("Vetor com 20 números aleatórios de 1 à 30:");
        for (int i = 0; i < 20; i++) {
            System.out.print(vetor[i] + " ");
            if (vetor[i] == 25) {
                found = true;
            }
        } if (found) {
            System.out.println("\nO número 25 existe no vetor.");
        } else {
            System.out.println("\nO número 25 não existe no vetor.");
        }
    }
}
# 5
import java.util.Random;
public class Main {
    public static void main(String[] args) {
        int[] vetor = new int[15];
        Random rand = new Random();
        boolean found = false;
        int index = -1;
        for (int i = 0; i < 15; i++) {
            vetor[i] = rand.nextInt(50) + 1; 
        } System.out.println("Vetor com 15 números aleatórios entre 1 e 50:");
        for (int i = 0; i < 15; i++) {
            System.out.print(vetor[i] + " ");
            if (vetor[i] == 20) {
                found = true;
                index = i;
            }
        } if (found) {
            System.out.println("\nO número 20 existe no vetor. Posição: " + index);
        } else {
            System.out.println("\nO número 20 não existe no vetor.");
        }
    }
}
# 6
import java.util.Scanner;
import java.util.Random;
public class Main {
    public static void main(String[] args) {
        int[] vetor = new int[30];
        Random rand = new Random();
        Scanner input = new Scanner(System.in);
        int valor;
        for (int i = 0; i < 30; i++) {
            vetor[i] = rand.nextInt(100) + 1; 
        } System.out.println("Vetor com 30 números aleatórios entre 1 e 100:");
        for (int i = 0; i < 30; i++) {
            System.out.print(vetor[i] + " ");
        } System.out.println("\nDigite um valor para procurar no vetor e remover:");
        valor = input.nextInt();
        boolean found = false;
        for (int i = 0; i < 30; i++) {
            if (vetor[i] == valor) {
                found = true;
                for (int j = i; j < 29; j++) {
                    vetor[j] = vetor[j + 1];
                } vetor[29] = 0;
                break;
            }
        } if (found) {
            System.out.println("O valor foi encontrado e removido.");
        } else {
            System.out.println("O valor não foi encontrado.");
        }
        System.out.println("\nVetor após remoção: ");
        for (int i = 0; i < 30; i++) {
            System.out.print(vetor[i] + " ");
        }
    }
}
# 7 
public class Main {
    public static void main(String[] args) {
        double[] vetor = new double[5];
        double maiorValor = Double.MIN_VALUE;
        double menorValor = Double.MAX_VALUE;
        for (int i = 0; i < 5; i++) {
            vetor[i] = i * 2.5; 
            if (vetor[i] > maiorValor) {
                maiorValor = vetor[i];
            } if (vetor[i] < menorValor) {
                menorValor = vetor[i];
            }
        } System.out.println("Vetor de 5 números decimais:");
        for (int i = 0; i < 5; i++) {
            System.out.print(vetor[i] + " ");
        } System.out.println("\nMaior valor no vetor: " + maiorValor);
        System.out.println("Menor valor no vetor: " + menorValor);
    }
}
# 8
public class Main {
    public static void main(String[] args) {
        int[] vetorA = new int[15];
        int[] vetorB = new int[15];
        for (int i = 0; i < 15; i++) {
            vetorA[i] = i + 1; 
        } for (int i = 0; i < 15; i++) {
            vetorB[i] = vetorA[14 - i];
        } System.out.println("Vetor A com 15 números inteiros:");
        for (int i = 0; i < 15; i++) {
            System.out.print(vetorA[i] + " ");
        } System.out.println("\nVetor B, cópia reversa de A:");
        for (int i = 0; i < 15; i++) {
            System.out.print(vetorB[i] + " ");
        }
    }
}
# 10
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Insira um número inteiro:");
        int num = input.nextInt();
        System.out.println("Tabuada do número " + num + ":");
        for (int i = 1; i <= 10; i++) {
            System.out.println(num + " x " + i + " = " + (num * i));
        }
    }
}
# 11
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        double[] temperatura = new double[10];
        double sum = 0;
        Scanner input = new Scanner(System.in);
        for (int i = 0; i < 10; i++) {
            System.out.print("Preencha com a temperatura da região " + (i + 1) + ": ");
            temperatura[i] = input.nextDouble();
            sum += temperatura[i];
        } double mediatemperatura = sum / 10;
        System.out.println("Temperatura média das regiões: " + mediatemperatura);
    }
}
