import java.util.Scanner;

public class Main {

    // Recursive function to convert string to integer
    public static int stringToInt(String str, int n) {
        // Base case: if the string is empty, return 0
        if (n == 0) {
            return 0;
        }

        // Get the last character and convert it to the corresponding integer
        int lastDigit = str.charAt(n - 1) - '0';

        // Recursive call to process the remaining part of the string
        return stringToInt(str, n - 1) * 10 + lastDigit;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Read the string input
        String str = scanner.nextLine();

        // Convert the string to integer
        int result = stringToInt(str, str.length());

        // Print the result
        System.out.println(result);

        // Close the scanner
        scanner.close();
    }
}
