# Car Rental System

## Overview

The Car Rental System is a Java-based application that allows users to rent and return cars. It utilizes Object-Oriented Programming (OOP) principles to manage the entities involved in the car rental process, including cars, customers, and rentals. The system provides a simple command-line interface for users to interact with.

## Features

- **Car Management**: Add and manage cars with details such as ID, brand, model, and base price per day.
- **Customer Management**: Register customers with unique IDs and names.
- **Rental Process**: Rent cars for a specified number of days and calculate the total rental price.
- **Return Process**: Return rented cars and update their availability status.
- **User  Interface**: A simple text-based menu for user interaction.

## Classes

### 1. `Car`
- Represents a car in the rental system.
- **Attributes**:
  - `carId`: Unique identifier for the car.
  - `brand`: Brand of the car.
  - `model`: Model of the car.
  - `basePricePerDay`: Rental price per day.
  - `isAvailable`: Availability status of the car.
- **Methods**:
  - `calculatePrice(int rentalDays)`: Calculates the total rental price based on the number of days.
  - `rent()`: Marks the car as rented.
  - `returnCar()`: Marks the car as available.

### 2. `Customer`
- Represents a customer in the rental system.
- **Attributes**:
  - `customerId`: Unique identifier for the customer.
  - `name`: Name of the customer.

### 3. `Rental`
- Represents a rental transaction.
- **Attributes**:
  - `car`: The car being rented.
  - `customer`: The customer renting the car.
  - `days`: Number of days for the rental.

### 4. `CarRentalSystem`
- Manages the overall functionality of the car rental system.
- **Attributes**:
  - `cars`: List of available cars.
  - `customers`: List of registered customers.
  - `rentals`: List of current rentals.
- **Methods**:
  - `addCar(Car car)`: Adds a car to the system.
  - `addCustomer(Customer customer)`: Adds a customer to the system.
  - `rentCar(Car car, Customer customer, int days)`: Processes the rental of a car.
  - `returnCar(Car car)`: Processes the return of a rented car.
  - `menu()`: Displays the main menu and handles user input.

## Getting Started

### Prerequisites

- Java Development Kit (JDK) installed on your machine.
- An IDE or text editor for Java development (e.g., IntelliJ IDEA, Eclipse, or Visual Studio Code).

### Installation

1. Clone the repository or download the source code.
2. Open the project in your preferred IDE.
3. Compile the Java files.
4. Run the `Main` class to start the Car Rental System.

### Usage

1. Upon running the application, you will see a menu with options to rent a car, return a car, or exit the system.
2. Follow the prompts to enter customer details, select a car, and specify rental days.
3. The system will display rental information and confirm the rental process.
4. You can return a car by providing the car ID.

## Example

```plaintext
===== Car Rental System =====
1. Rent a Car
2. Return a Car
3. Exit
Enter your choice: 1

== Rent a Car ==

Enter your name: Rohit Sharma

Available Cars:
C001 - Suzuki Fronx
C002 - Hyundai Venue
C003 - Hyundai i20

Enter the car ID you want to rent: C001
Enter the number of days for rental: 3

== Rental Information ==

Customer ID: C001
Customer Name: John Doe
Car: Suzuki Fronx
Rental Days: 3
Total Price: Rs.5700.00

Confirm rental (Y/N): Y
Car rented successfully.