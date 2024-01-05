import java.util.Random;
import java.util.Scanner;

class Main {
    private static final Random r = new Random();
    private static final int NUMBER = r.nextInt(100) + 1;
    private static int guess = 0;

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        while (guess != NUMBER) {
            System.out.println("Guess a number between 1 and 100");
            guess = sc.nextInt();
            if (guess == -1) {
                System.out.println("number is " + String.valueOf(NUMBER));
            }
            if (guess > NUMBER) {
                System.out.println("Too high");
            } else if (guess < NUMBER) {
                System.out.println("Too low");
            } else {
                System.out.println("That's right!");
                System.exit(0);
            }
        }
    }
}
