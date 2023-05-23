# Online-Reservation-System
//Task1 of Java Programming
package onlineReservationSystem;

import java.util.Scanner;

public class OnlineReservationSystem {
    public static void main(String[] args) {
        OnlineReservationSystem reservationSystem = new OnlineReservationSystem();
        reservationSystem.run();
    }

    public void run() {
        Scanner scanner = new Scanner(System.in);
        boolean loggedIn = false;
        int choice;

        while (true) {
            System.out.println("Welcome to the Online Reservation System");
            System.out.println("----------------------------------------");
            System.out.println("1. Login");
            System.out.println("2. Exit");
            System.out.print("Enter your choice: ");
            choice = scanner.nextInt();

            switch (choice) {
                case 1:
                    loggedIn = loginForm();
                    break;
                case 2:
                    System.out.println("Exiting the system...");
                    return;
                default:
                    System.out.println("Invalid choice. Please try again.");
                    break;
            }

            if (loggedIn) {
                break;
            }
        }

        while (loggedIn) {
            System.out.println("Online Reservation System");
            System.out.println("--------------------------");
            System.out.println("1. Reservation System");
            System.out.println("2. Cancellation Form");
            System.out.println("3. Ticket Status");
            System.out.println("4. Train Schedule");
            System.out.println("5. Availability");
            System.out.println("6. Fare Enquiry");
            System.out.println("7. Payment");
            System.out.println("8. Logout");
            System.out.print("Enter your choice: ");
            choice = scanner.nextInt();

            switch (choice) {
                case 1:
                    reservationSystem();
                    break;
                case 2:
                    cancellationForm();
                    break;
                case 3:
                    ticketStatus();
                    break;
                case 4:
                    trainSchedule();
                    break;
                case 5:
                    availability();
                    break;
                case 6:
                    fareEnquiry();
                    break;
                case 7:
                    payment();
                    break;
                case 8:
                    System.out.println("Logging out...");
                    loggedIn = false;
                    break;
                default:
                    System.out.println("Invalid choice. Please try again.");
                    break;
            }
        }
    }

    private void availability() {
		
		
	}

	private void fareEnquiry() {
	
		
	}

	private void payment() {
		
		
	}

	public boolean loginForm() {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Login Form");
        System.out.print("Enter your username: ");
        String username = scanner.nextLine();
        System.out.print("Enter your password: ");
        String password = scanner.nextLine();

        
        boolean authenticated = authenticateUser(username, password);

        if (authenticated) {
            System.out.println("Login successful!");
            return true;
        } else {
            System.out.println("Invalid username or password. Please try again.");
            return false;
        }
    }

    private boolean authenticateUser(String username, String password) {
		
		return false;
	}

	public void reservationSystem() {
        
        System.out.println("Reservation System");
    }

    public void cancellationForm() {
        
        System.out.println("Cancellation Form");
    }

    public void ticketStatus() {
        
        System.out.println("Ticket Status");
    }

    public void trainSchedule() {
        
        System.out.println("Train Schedule");
    }
}

