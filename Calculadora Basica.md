package tarea2;

import java.util.Scanner;

public class Tarea2IPC {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double num1, num2;
        char operador;

        System.out.println("Ingrese el primer número:");
        num1 = scanner.nextDouble();

        System.out.println("Ingrese el operador (+, -, *, /):");
        operador = scanner.next().charAt(0);

        System.out.println("Ingrese el segundo número:");
        num2 = scanner.nextDouble();

        double resultado = 0;
        switch (operador) {
            case '+':
                resultado = num1 + num2;
                break;
            case '-':
                resultado = num1 - num2;
                break;
            case '*':
                resultado = num1 * num2;
                break;
            case '/':
                if (num2 != 0) {
                    resultado = num1 / num2;
                } else {
                    System.out.println("Error: No se puede dividir por cero.");
                    return;
                }
                break;
            default:
                System.out.println("Operador no válido.");
                return;
        }
        System.out.println("El resultado es: " + resultado);
    }
}
