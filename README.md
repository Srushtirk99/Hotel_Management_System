
# Hotel Management System

## Overview
This Hotel Management System is a C++ program that uses Object-Oriented Programming (OOP) concepts to manage hotel bookings, check-ins, check-outs, and room statuses. It ensures efficient hotel operations while maintaining customer details and billing information.

## OOP Concepts Used

1. **Encapsulation** - Data members (e.g., customer details, room status) are encapsulated within classes.
2. **Abstraction** - The `Person` class is an abstract base class with a pure virtual function `displayDetails()`.
3. **Inheritance** - `Customer` class inherits from the `Person` class.
4. **Polymorphism** - The `displayDetails()` method is overridden in the `Customer` class.
5. **Operator Overloading** - The `>` operator is overloaded to compare customer loyalty points.
6. **Static Members** - `totalBookings` is a static member to track total hotel bookings.
7. **Exception Handling & Validation** - Phone number validation is implemented using regular expressions.

## Functionalities

### ✅ Booking a Room
- Takes customer details (name, phone number, room number, stay duration, and room type).
- Checks if the room is available.
- Calculates bill and adds loyalty points.
- Saves the customer details.

### ✅ Displaying Customers
- Shows a list of all booked customers with their details (name, room number, room type, stay duration, bill amount, and loyalty points).

### ✅ Checking Out
- Takes the room number.
- Displays bill and prompts payment.
- If payment is insufficient, an error message is displayed.
- Marks the room as needing cleaning after checkout.

### ✅ Displaying Room Status
- Shows the status of all rooms (either occupied or needing cleaning).

## Sample Inputs and Outputs

### ✅ Successful Room Booking
#### **Input:**
```
Enter Customer Name: Srushti
Enter Phone Number (10 digits): 9876543210
Enter Room Number: 101
Enter Stay Duration (nights): 3
Select Room Type:
1️⃣ Single - $100/night
2️⃣ Double - $150/night
3️⃣ Suite - $250/night
Enter choice: 2
```
#### **Output:**
```
✅ Room booked successfully for Srushti!
```

---

### ❌ Room Booking with Invalid Phone Number
#### **Input:**
```
Enter Customer Name: teju
Enter Phone Number (10 digits): 12345
```
#### **Output:**
```
❌ Invalid phone number! Please enter exactly 10 digits.
```

---

### ❌ Room Already Booked
#### **Input:**
```
Enter Room Number: 101
```
#### **Output:**
```
❌ Room already booked!
```

---

### ✅ Successful Checkout with Full Payment
#### **Input:**
```
Enter Room Number to Check Out: 101
💳 Enter payment amount: $450
```
#### **Output:**
```
✅ Payment successful!
✅ Check-out successful.
Room needs cleaning.
```

---

### ❌ Checkout with Insufficient Payment
#### **Input:**
```
Enter Room Number to Check Out: 101
💳 Enter payment amount: $200
```
#### **Output:**
```
❌ Insufficient amount. Please pay the full bill: $450.00
```

---

### ✅ Displaying Room Status
#### **Output:**
```
🛏️ Room Status:
Room 102: ✅ Occupied
```

---

## Future Improvements
- Implement a database for persistent storage.
- Add more room features (e.g., amenities selection).
- Introduce a graphical user interface (GUI) using Qt or another framework.
- Implement automatic discount calculation based on loyalty points.

## How to Run
1. Clone the repository:
```
git clone https://github.com/Srushtirk99/Hotel_Management_System.git
```
2. Compile the code using g++:
```
g++ Hotel_Management_System.cpp -o Hotel_Management_System
```
3. Run the executable:
```
./Hotel_Management_System
```

Enjoy managing your hotel with this system! 🚀

