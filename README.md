## Car Rental System in Java - Detailed and Interactive Guide

This **Car Rental System** project is a console-based application implemented in Java. It allows customers to rent and return cars from a list of available vehicles. Let's break down the various components of the system and understand how they work together.

### Project Structure

- **Car Class**: Represents individual cars available for rent.
- **Customer Class**: Represents customers who rent cars.
- **Rental Class**: Tracks information about rentals, connecting customers and cars.
- **CarRentalSystem Class**: Manages the overall system including cars, customers, and rentals.
- **Main Class**: Entry point of the application that starts the Car Rental System and adds initial data.

### Key Features

1. **Car Renting**:
   - Displays available cars.
   - Takes customer details and allows them to rent a car for a specified number of days.
   - Calculates and displays the total rental price based on the daily rate and number of days.
   - Marks the car as rented.

2. **Car Returning**:
   - Allows customers to return previously rented cars by providing the car ID.
   - Marks the car as available again for future rentals.

3. **Car Availability**:
   - Cars that are rented are marked as unavailable, preventing them from being rented again until returned.

### Detailed Breakdown of Each Class

#### 1. **Car Class**

This class represents individual cars available for rent. It has attributes like car ID, brand, model, price per day, and availability status.

- **Fields**:
  - `carId`: Unique ID of the car.
  - `brand`: Brand of the car (e.g., Toyota).
  - `model`: Model of the car (e.g., Fortuner).
  - `basePricePerDay`: The rental price per day.
  - `isAvailable`: Whether the car is available for rent.

- **Methods**:
  - `rent()`: Marks the car as unavailable when rented.
  - `returnCar()`: Marks the car as available when returned.
  - `calculatePrice(int days)`: Calculates the total rental price for the given number of days.

#### 2. **Customer Class**

This class represents a customer in the system. It contains basic information like customer ID and name.

- **Fields**:
  - `customerId`: Unique ID of the customer.
  - `name`: Name of the customer.

#### 3. **Rental Class**

This class connects a customer with a car for a rental. It stores details about the rental, including which car was rented, by whom, and for how long.

- **Fields**:
  - `car`: The car being rented.
  - `customer`: The customer renting the car.
  - `days`: The number of days the car is rented for.

#### 4. **CarRentalSystem Class**

This class manages the list of cars, customers, and rentals. It provides the main functionality for renting and returning cars and handles the user interactions.

- **Fields**:
  - `cars`: A list of cars available in the system.
  - `customers`: A list of customers who have rented cars.
  - `rentals`: A list of active rentals.

- **Methods**:
  - `addCar(Car car)`: Adds a new car to the system.
  - `addCustomer(Customer customer)`: Adds a new customer to the system.
  - `rentCar(Car car, Customer customer, int days)`: Rents a car to a customer for the given number of days.
  - `returnCar(Car car)`: Returns a rented car and marks it as available.
  - `menu()`: The interactive menu for the car rental system, allowing users to rent or return cars.

#### 5. **Main Class**

This class initializes the system, adds some default cars, and starts the user interaction.

### Running the System

When you run the system, the following steps occur:

1. **Initialize the System**: The system is initialized with some default cars, such as Toyota Fortuner, Suzuki Swift, etc.
2. **Display Menu**: The main menu is displayed with options to rent a car, return a car, or exit the system.

### Interactive Guide

1. **Rent a Car**:
   - The system asks for the customer’s name.
   - It displays all available cars.
   - The customer selects a car by entering its ID and specifies the number of rental days.
   - The system calculates the total price and asks for confirmation before renting.
   - If confirmed, the car is rented and marked as unavailable.

2. **Return a Car**:
   - The system asks for the car ID.
   - If the car was rented, it is marked as available again.
   - If the car was not rented, an appropriate message is displayed.

3. **Exit**:
   - The system will terminate when the user selects the exit option.

### Example Interaction

```plaintext
====== Car Rental System ======
 1. Rent a Car
 2. Return a Car
 3. Exit
Enter a choice: 1

== Rent a car ==

Enter your name: John Doe

Available cars:
C001 - Toyota Fortuner
C002 - Suzuki Swift
C003 - Mahindra Thar
C004 - Tata Nexon
C005 - Hyundai Creta

Enter the car ID you want to rent: C001
Enter the number of days for rental: 5

== Rental Information ==
Customer ID: CUS1
Customer Name: John Doe
Car: Toyota Fortuner
Rental Days: 5
Total Price: $2500.00

Confirm rental (Y/N): Y

Car rented successfully.
```

In this interaction, a customer named John Doe rents a Toyota Fortuner for 5 days, and the system confirms the rental with a total price of $2500. 

---
