/* John Renzel M. Fangon 
/* CC2 1B

import java.util.Scanner;

public class RestaurantOrderSystem {

    public static void main(String[] args) {
        
        // Create a Scanner object to take input from the user
        Scanner scanner = new Scanner(System.in);

        // Menu display
        System.out.println("MENU");
        System.out.println("1. Burger    - PHP 100");
        System.out.println("2. Fries     - PHP 50");
        System.out.println("3. Soda      - PHP 30");
        System.out.println("4. Ice Cream - PHP 45");
        System.out.println("5. Exit");

        // Variable to track the total cost
        double totalAmount = 0.0;

        while (true) {
            // Prompt the user to select an item
            System.out.print("\nEnter the menu number of your choice: ");
            int choice = scanner.nextInt();

            // If the user chooses to exit, break out of the loop
            if (choice == 5) {
                break;
            }

            // Ask the user for the quantity
            System.out.print("Enter the quantity: ");
            int quantity = scanner.nextInt();

            // Use switch statement to calculate the total for the selected item
            switch (choice) {
                case 1:
                    totalAmount += 100 * quantity; // Burger price
                    System.out.println("You ordered Burger.");
                    break;
                case 2:
                    totalAmount += 50 * quantity; // Fries price
                    System.out.println("You ordered Fries.");
                    break;
                case 3:
                    totalAmount += 30 * quantity; // Soda price
                    System.out.println("You ordered Soda.");
                    break;
                case 4:
                    totalAmount += 45 * quantity; // Ice Cream price
                    System.out.println("You ordered Ice Cream.");
                    break;
                default:
                    System.out.println("Invalid choice. Please select a valid menu number.");
                    continue;
            }

            // Display the total amount after each item
            System.out.println("Total amount: PHP " + totalAmount);
        }

        // Display the final total amount
        System.out.println("\nFinal total bill: PHP " + totalAmount);

        // Close the scanner object
        scanner.close();
    }
}
