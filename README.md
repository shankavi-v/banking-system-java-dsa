# Banking Transaction Management System

A desktop banking application built with **Java Swing** for the BTEC HND Computing (Software Engineering) Unit 19 – Data Structures & Algorithms. It demonstrates how core data structures are applied in a real-world banking workflow, with a maroon and gold themed UI.

## Features

- Sign up and login
- Create, update and close bank accounts
- Deposit, withdraw and transfer funds
- Undo the last transaction
- Edit user profile
- Dashboard menu linking all screens

## Data Structures Used

| Structure | Where it is used |
|---|---|
| Singly linked list (custom `AccountList`) | Storing and managing bank accounts |
| Generic stack (custom `Stack<T>`) | Undo transaction history (LIFO) |
| Queue (`LinkedList`) | Normal customer requests (FIFO) |
| Priority queue (`PriorityQueue`) | VIP customer requests |

## Algorithm Demos

- `LinearSearchDemo.java` – counts comparisons to show **O(n)** growth
- `BinarySearchDemo.java` – counts comparisons to show **O(log n)** growth

## Project Structure

```
src/banking/
├── Main.java              # Entry point (opens Sign Up)
├── BankData.java          # Shared backend: data structures and file storage
├── Theme.java             # Maroon & gold styling helpers
├── IconFactory.java       # Vector-drawn icons (Graphics2D)
├── SignUpFrame.java / LoginFrame.java / DashboardFrame.java
├── CreateAccountFrame.java / UpdateAccountFrame.java / CloseAccountFrame.java
├── DepositFrame.java / WithdrawFrame.java / TransferFrame.java
├── UndoFrame.java / EditProfileFrame.java
├── LinearSearchDemo.java / BinarySearchDemo.java
```

## How to Run

**Requirements:** JDK 17 or later.

From the project root:

```bash
mkdir out
javac -d out src/banking/*.java
java -cp out banking.Main
```

**Using NetBeans:** create a new *Java with Ant → Java Application* project, copy the files from `src/banking/` into its `src/banking/` folder, then right-click `Main.java` → *Run File*.

## Notes

- Data is saved to `users_details.txt` and `accounts_data.txt` in the working directory. These are git-ignored because they contain user data.
- This is an academic project. Passwords are stored in plain text for simplicity and should never be used like this in production.

## Author

**Shankavi Vigneswaran**
BSc (Hons) Computer Science in Software Engineering, Goldsmiths, University of London (via BCAS Campus, Jaffna)
