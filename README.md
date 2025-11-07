# 📚 Library Management System 

A simple yet functional **Library Management System** built in Python that uses **CSV files** for data persistence.  
It allows librarians and users to **manage books, register users, borrow and return books**, and automatically handles **fine calculation** after a configurable grace period.

---

## 🚀 Features

✅ **Core Features**
- Add, list, and search books by title.  
- Register new users.  
- Borrow and return books with automatic quantity updates.  
- View all borrowed books by a specific user.  
- Fine calculation for overdue returns.

✅ **Advanced Features**
- Persistent data storage using **CSV files** (`books.csv`, `users.csv`, `borrows.csv`).
- Optimized lookups using **Python dictionaries (O(1))** instead of lists (O(n)).
- Configurable system settings:
  - `max_borrow_per_user` — maximum books one user can borrow.
  - `bookkeeping_days` — grace period (no fine within this many days).
  - `fine_rate_per_day` — fine amount (in ₹ or $) per overdue day.
- Handles edge cases:
  - Duplicate book or user IDs.
  - Borrowing unavailable books.
  - Borrowing the same book twice.
  - Borrowing limit exceeded.
  - Returning un-borrowed books.

---

## 🧠 Project Overview

The system maintains three core data entities:

| Class | Description |
|--------|-------------|
| `Book` | Represents each book with `book_id`, `title`, `author`, and `quantity`. |
| `User` | Represents a user with `user_id`, `name`, and a list of borrowed books. |
| `BorrowRecord` | Stores details of each borrow transaction (date, returned status, fine). |

All these are managed by the `Library` class, which coordinates between them and handles persistence.

---

## 🧩 File Structure

LibraryManagementSystem/
|
├── library_management.py # Main Python code (your script)
├── books.csv # Stored book data
├── users.csv # Stored user data
├── borrows.csv # Borrow and return records
└── README.md # Project documentation


