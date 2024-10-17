import java.util.HashSet;
import java.util.Scanner;

public class HappyNumber {

    public static boolean isHappyNumber(int num) {
        HashSet<Integer> seenNumbers = new HashSet<>();
        
        while (num != 1 && !seenNumbers.contains(num)) {
            seenNumbers.add(num);
            num = sumOfSquaresOfDigits(num);
        }
        
        return num == 1;
    }

    public static int sumOfSquaresOfDigits(int num) {
        int sum = 0;
        while (num > 0) {
            int digit = num % 10;
            sum += digit * digit;
            num /= 10;
        }
        return sum;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int number = scanner.nextInt();

        if (isHappyNumber(number)) {
            System.out.println(number + " is a happy number.");
        } else {
            System.out.println(number + " is not a happy number.");
        }
        
        scanner.close();
    }
}
