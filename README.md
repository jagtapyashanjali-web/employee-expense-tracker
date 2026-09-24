# Employee Expense Tracker

A simple command-line/notebook-based expense tracking system built with Python, SQLite, and Pandas. It allows users to record, view, search, update, and delete employee expenses, along with generating quick summaries and category-wise reports.

## Features

- **Add Expense** – Record a new expense with date, category, description, amount, and payment method.
- **Bulk Add** – Insert multiple expenses at once.
- **View All Expenses** – Display all recorded expenses in a table format (via Pandas DataFrame).
- **Search by Category** – Filter and view expenses belonging to a specific category (e.g., Food, Travel).
- **Total Expenses** – Calculate the sum of all recorded expenses.
- **Category-wise Summary** – Get a breakdown of total spending per category.
- **Update Expense** – Modify the amount of an existing expense by ID.
- **Delete Expense** – Remove an expense record by ID.

## Tech Stack

- **Python 3**
- **SQLite3** – lightweight relational database for persistent storage
- **Pandas** – for tabular data display and analysis

## How It Works

The project uses an SQLite database (`expense_tracker.db`) with a single `expenses` table containing:

| Column | Type | Description |
|---|---|---|
| id | INTEGER (Primary Key) | Auto-incrementing unique ID |
| date | TEXT | Date of the expense |
| category | TEXT | Expense category (e.g., Food, Travel) |
| description | TEXT | Short description of the expense |
| amount | REAL | Expense amount |
| payment_method | TEXT | Mode of payment (e.g., UPI, Cash) |

Each operation (add, view, search, update, delete) is performed using standard SQL queries executed through Python's `sqlite3` module, with results displayed either as raw tuples or formatted Pandas DataFrames.

## How to Run

1. Open the notebook (`Employee_Expense_Tracker.ipynb`) in Google Colab or Jupyter Notebook.
2. Run the cells in order from top to bottom.
3. Each cell demonstrates a specific operation (add, view, search, total, update, delete).

## Sample Output
Total Expenses: ₹ 2840.0
Food → ₹ 800.0
Travel → ₹ 240.0
Shopping → ₹ 1600.0
Education → ₹ 200.0
