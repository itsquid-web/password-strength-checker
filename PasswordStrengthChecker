import java.util.Scanner;

public class PasswordStrengthChecker {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        boolean running = true;

        while (running) {
            System.out.println("\n=== Password Strength Checker ===");
            System.out.println("1. Check Password");
            System.out.println("2. Exit");
            System.out.print("Choose an option: ");

            String choice = scanner.nextLine();

            if (choice.equals("1")) {
                System.out.print("Enter password: ");
                String password = scanner.nextLine();

                int score = 0;

                if (password.length() >= 8) score++;
                if (password.matches(".*[A-Z].*")) score++;
                if (password.matches(".*[a-z].*")) score++;
                if (password.matches(".*\\d.*")) score++;
                if (password.matches(".*[^a-zA-Z0-9].*")) score++;

                String strength;
                if (score <= 2) {
                    strength = "Weak";
                } else if (score <= 4) {
                    strength = "Medium";
                } else {
                    strength = "Strong";
                }

                System.out.println("Strength: " + strength);
                giveFeedback(password);

            } else if (choice.equals("2")) {
                running = false;
                System.out.println("Exiting program...");
            } else {
                System.out.println("Invalid choice. Please try again.");
            }
        }

        scanner.close();
    }

    public static void giveFeedback(String password) {
        if (password.length() < 8) {
            System.out.println("- Use at least 8 characters");
        }
        if (!password.matches(".*[A-Z].*")) {
            System.out.println("- Add an uppercase letter");
        }
        if (!password.matches(".*[a-z].*")) {
            System.out.println("- Add a lowercase letter");
        }
        if (!password.matches(".*\\d.*")) {
            System.out.println("- Add a number");
        }
        if (!password.matches(".*[^a-zA-Z0-9].*")) {
            System.out.println("- Add a special character");
        }
    }
}
