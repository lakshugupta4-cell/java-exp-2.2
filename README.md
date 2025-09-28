# java-exp-2.2
import java.util.Scanner;

public class BalancedNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String n = sc.next();  // Read input as string
        sc.close();

        int sumOdd = 0;
        int sumEven = 0;

        for (int i = 0; i < n.length(); i++) {
            int digit = n.charAt(i) - '0';
            if ((i + 1) % 2 == 1) {
                sumOdd += digit;    // 1-based odd positions
            } else {
                sumEven += digit;   // 1-based even positions
            }
        }

        if (sumOdd == sumEven) {
            System.out.println("Balanced");
        } else {
            System.out.println("Not Balanced");
        }
    }
}
