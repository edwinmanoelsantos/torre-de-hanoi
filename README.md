# torre-de-hanoi

import java.util.Scanner;

public class Hanoi {

	private static void mover(int O, int D) {
		System.out.println(O + " -> " + D);
	}

	static void hanoi(int n, int O, int D, int T) {

		if (n > 0) {
			hanoi(n - 1, O, T, D);
			mover(O, D);
			hanoi(n - 1, T, D, O);
		}

	}

	public static void main(String[] args) {

		int n; 
		Scanner entrada = new Scanner(System.in);
		System.out.println("Digite o número de discos: ");
		n = entrada.nextInt();

		Hanoi.hanoi(n, 1, 3, 2);
	}
}
