# Reverse-masiv-N-chisla
import java.util.Scanner;

public class Zadacha2 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

		System.out.println("Въведете N");
		Scanner in = new Scanner(System.in);
		int n = in.nextInt();
		int[] numbers = new int[n];

		for (int i = 0; i < numbers.length; i++) {
			numbers[i] = in.nextInt();
		}
		System.out.println("Преди обръщане:");
		print(numbers);
		reverse(numbers);

		System.out.println("\nСлед обръщане:");
		print(numbers);
	}

	static void reverse(int[] numbers) {
		for (int i = 0; i < numbers.length / 2; i++) {
			int temp = numbers[i];
			numbers[i] = numbers[numbers.length - 1 - i];
			numbers[numbers.length - 1 - i] = temp;
		}

	}

	static void print(int[] arr) {
		for (int i = 0; i < arr.length; i++) {
			System.out.print(arr[i] + " ");
		}
	}
}
