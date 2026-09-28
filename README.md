# Smart_Daily_Expense_Tracker_VITYARTHI_PROJECT
## 1. Project Overview

The **Smart Daily Expense Tracker** is a Python-based command-line application developed for CSE1012. It helps a user record and manage daily expenses in a simple and organized way.

The project stores every expense using three values:

`(category, amount, date)`

The application can add, display, search, delete and analyse expense records. Data is stored locally in a JSON file so that saved expenses remain available when the program is opened again.

## 2. Problem Statement

Managing small daily expenses manually can make it difficult to know where money is being spent. The purpose of this project is to provide a simple program that records expenses and automatically produces useful summaries.

## 3. Objectives

- Record daily expenses in a structured format.
- Allow users to view and search stored expenses.
- Allow incorrect records to be rejected through validation.
- Calculate total spending.
- Generate category-wise spending summaries.
- Generate daily spending summaries.
- Identify the category with the highest spending.
- Save data permanently using JSON storage.
- Demonstrate Python programming concepts through a practical application.

## 4. Main Features

1. **Add Expense** – Enter category, amount and date.
2. **View All Expenses** – Display all saved records.
3. **Search by Category** – Find expenses belonging to a selected category.
4. **Category-wise Summary** – Calculate total spending for every category.
5. **Daily Summary** – Calculate spending for each date.
6. **Highest Spending Category** – Find the category with the highest total expenditure.
7. **Delete Expense** – Remove an unwanted expense record.
8. **Total Spending** – Calculate the overall amount spent.
9. **JSON Persistence** – Save and reload expense data automatically.
10. **Validation and Error Handling** – Prevent invalid amounts, empty categories and incorrect dates.

## 5. Functional Requirements

- The system shall accept an expense category.
- The system shall accept a positive numerical amount.
- The system shall accept dates in `DD-MM-YYYY` format.
- The system shall store each valid expense.
- The system shall display stored expenses.
- The system shall search expenses by category.
- The system shall calculate category-wise totals.
- The system shall calculate daily totals.
- The system shall calculate total spending.
- The system shall delete a selected expense.

## 6. Non-Functional Requirements

- **Usability:** The menu should be simple for a beginner to understand.
- **Reliability:** Invalid input should not crash the application.
- **Maintainability:** The program is organized into separate modules.
- **Performance:** Expense calculations should complete quickly for normal student-level datasets.
- **Data Persistence:** Saved expenses should remain available after restarting the program.
- **Error Handling:** Invalid input should produce a clear error message.

## 7. Python Concepts Used

This project demonstrates:

- Variables and data types
- Lists
- Tuples
- Dictionaries
- `for` and `while` loops
- `if-elif-else` statements
- Functions
- Function parameters and return values
- Modules and imports
- Exception handling using `try-except`
- File handling
- JSON data handling
- Date validation using `datetime`
- Automated testing

## 8. Program Architecture

The application follows a modular structure:

```text
User
  ↓
main.py
  ↓
menu.py
  ↓
expense_manager.py
  ├── validators.py
  ├── reports.py
  └── storage.py
          ↓
    data/expenses.json
```

### Module Responsibilities

- **main.py:** Starts the application.
- **menu.py:** Displays the menu and handles user interaction.
- **expense_manager.py:** Controls expense operations.
- **validators.py:** Checks category, amount and date input.
- **reports.py:** Performs calculations and generates summaries.
- **storage.py:** Reads and writes expense data to JSON.
- **utils.py:** Provides formatting and display helper functions.

## 9. Input and Output

### Example Input

```text
Category: Food
Amount: 150
Date: 26-09-2026
```

### Example Stored Record

```text
('Food', 150.0, '26-09-2026')
```

### Example Output

```text
Food | ₹150.00 | 26-09-2026

Total Spending: ₹150.00
```

## 10. Validation Rules

The program checks the following conditions:

- Category cannot be empty.
- Amount must be numeric.
- Amount must be greater than zero.
- Date must follow `DD-MM-YYYY` format.
- An invalid expense number cannot be deleted.
- Invalid menu choices are rejected.

## 11. Data Storage

Expense records are stored in:

```text
data/expenses.json
```

JSON is used because it is lightweight, human-readable and available through Python's standard library.

The program loads existing records when it starts and saves changes after adding or deleting an expense.

## 12. Project Structure

```text
Smart_Daily_Expense_Tracker/
├── main.py
├── Smart_Daily_Expense_Tracker.py
├── expense_manager.py
├── storage.py
├── validators.py
├── reports.py
├── menu.py
├── utils.py
├── requirements.txt
├── statement.md
├── README.md
├── data/
│   └── expenses.json
├── tests/
│   └── test_expense_tracker.py
└── report/
    └── Project_Report.pdf
```

The modular files demonstrate separation of responsibilities. The standalone `Smart_Daily_Expense_Tracker.py` file contains the combined version when a submission portal accepts only one Python file.

## 13. Setup and Execution

### Requirements

- Python 3.8 or later
- No third-party Python packages are required for the main application.

### Run the modular version

Open a terminal in the project folder and run:

```bash
python main.py
```

### Run the standalone version

```bash
python Smart_Daily_Expense_Tracker.py
```

## 14. Testing

The project includes automated tests for validation and report calculations.

Run the tests with:

```bash
python -m unittest discover -s tests -p "test_*.py" -v
```

Important test areas include:

- Valid category input
- Invalid amount handling
- Valid date handling
- Invalid date handling
- Category summary calculation
- Daily summary calculation
- Highest spending category
- Total spending calculation

## 15. Typical User Workflow

```text
Start Program
     ↓
Display Main Menu
     ↓
Choose an Operation
     ↓
Enter / View / Search / Delete Data
     ↓
Validate Input
     ↓
Process Expense
     ↓
Save Changes to JSON
     ↓
Display Result
     ↓
Return to Menu
     ↓
Exit
```

## 16. Design Decisions

- **Tuples** are used to represent individual expense records as `(category, amount, date)`.
- **Lists** store multiple expense records.
- **Dictionaries** are used for category-wise and daily summaries.
- **JSON** is used for simple local persistence without requiring a database.
- **Separate modules** make the code easier to understand, test and maintain.
- **Validation functions** keep input checking separate from business logic.

## 17. Limitations

- The application is command-line based.
- It currently supports one local expense dataset.
- It does not require user accounts or cloud synchronization.
- It does not provide graphical charts.

## 18. Future Enhancements

Possible future improvements include:

- Graphical user interface using Tkinter.
- Monthly and weekly reports.
- Budget-limit alerts.
- Expense charts and visual analytics.
- Export reports to CSV or PDF.
- Multiple user profiles.
- Cloud/database storage.
- Edit/update existing expenses.

## 19. Learning Outcomes

By completing this project, the student demonstrates practical understanding of Python fundamentals, modular programming, data structures, file handling, JSON, validation, exception handling and testing.

## 20. Before Submission

- Run the project yourself.
- Add realistic test expenses.
- Capture screenshots of the program output.
- Check that the screenshots are your own.
- Run the test suite and verify that it passes.
- Read and understand each major module before the viva.
- Add the screenshots and any required college-specific information to the final report.

## 21. Academic Note

This project is intended as an individual academic implementation. The student should understand the code, test the application personally and make any changes required by the course or faculty before submission.