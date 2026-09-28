SMART DAILY EXPENSE TRACKER

1. Project Overview

The Smart Daily Expense Tracker is a Python-based console application developed to help users record, manage, search, and analyze their daily expenses in a simple and organized manner. The main purpose of this project is to provide an easy-to-use system through which users can maintain their personal spending records without relying on manual calculations or paper-based records.

Managing daily expenses is an important part of personal financial management. Small expenses made throughout the day can be difficult to remember and calculate accurately. This project addresses this problem by providing a structured application where each expense is stored along with its category, amount, and date. The application also provides useful summaries that allow users to understand their spending patterns.

The project is implemented using Python and makes use of fundamental programming concepts such as functions, lists, tuples, dictionaries, loops, conditional statements, exception handling, file handling, JSON data storage, and input validation.

The application stores expense information in a local JSON file named expenses.json. This allows the data to remain available even after the program is closed and restarted. The program follows a menu-driven approach, allowing the user to select different operations according to their requirements.

⸻

2. Problem Statement

Keeping track of daily expenses manually can become difficult when the number of transactions increases. Users may forget individual expenses, make calculation errors, or find it difficult to determine which category consumes the most money.

A simple expense management system is therefore required to:

* Record individual expenses.
* Store the category of each expense.
* Store the amount spent.
* Record the date of the expense.
* Display all stored expenses.
* Search expenses according to category.
* Calculate category-wise spending.
* Calculate daily spending.
* Identify the category with the highest spending.
* Calculate total expenditure.
* Delete incorrect or unwanted expense records.
* Store the data permanently for future use.

The Smart Daily Expense Tracker is designed to satisfy these requirements through a simple command-line interface.

⸻

3. Objectives

The main objectives of this project are:

1. To develop a simple Python application for recording daily expenses.
2. To provide an organized way of storing expense information.
3. To reduce manual calculations related to personal spending.
4. To implement input validation for categories, amounts, and dates.
5. To provide category-wise and date-wise expense summaries.
6. To identify the category in which the user spends the most money.
7. To allow users to search for expenses based on categories.
8. To allow users to delete unwanted expense records.
9. To calculate and display the total amount spent.
10. To use JSON-based file handling for persistent data storage.
11. To apply fundamental programming concepts learned in the course to a practical problem.

⸻

4. Features of the Application

The application provides a menu containing nine different options.

4.1 Add Expense

The Add Expense feature allows the user to enter three important pieces of information:

* Category
* Amount
* Date

For example, a user can enter:

Category: Food
Amount: 150
Date: 28-09-2026

After successful validation, the expense is added to the list and saved to the JSON file.

⸻

4.2 View All Expenses

The View All Expenses option displays every expense currently stored in the application.

Each expense is displayed with:

* Expense number
* Category
* Amount
* Date

For example:

1. Food | ₹150.00 | 28-09-2026
2. Transport | ₹80.00 | 28-09-2026
3. Books | ₹500.00 | 27-09-2026

This provides the user with a complete view of their recorded transactions.

⸻

4.3 Search by Category

The application allows users to search for expenses using a category name.

For example, if the user searches for Food, the application displays only the expenses associated with that category.

The search operation is case-insensitive, meaning that inputs such as Food, food, and FOOD can be matched with the same category.

⸻

4.4 Category-wise Summary

The Category-wise Summary feature calculates the total amount spent under each category.

For example:

Food: ₹850.00
Transport: ₹400.00
Books: ₹1200.00
Entertainment: ₹500.00

This helps users understand how their total spending is distributed among different categories.

The summary is generated using a Python dictionary, where the category acts as the key and the total amount acts as the value.

⸻

4.5 Daily Summary

The Daily Summary feature calculates the total expenditure for each date.

For example:

27-09-2026: ₹750.00
28-09-2026: ₹1250.00

This allows the user to identify how much money was spent on individual days.

⸻

4.6 Highest Spending Category

The application can identify the category in which the user has spent the highest total amount.

For example:

Highest spending category: Books
Amount spent: ₹1200.00

This information can help users recognize categories that contribute significantly to their overall expenditure.

⸻

4.7 Delete Expense

The Delete Expense option allows the user to remove a particular expense from the stored list.

The program first displays all expenses with their corresponding numbers. The user can then enter the number of the expense that should be deleted.

After deletion, the updated list is automatically saved to the JSON file.

⸻

4.8 Total Spending

The Total Spending option calculates the total amount of all recorded expenses.

For example:

Total Spending: ₹3000.00

This is calculated by adding the amount of every stored expense.

⸻

4.9 Exit

The Exit option terminates the application safely and displays a thank-you message.

⸻

5. Implementation Details

The project is implemented using Python’s built-in modules.

The following modules are used:

json

The json module is used to store and retrieve expense information from the expenses.json file.

os

The os module is used to construct the file path and check whether the data file exists.

datetime

The datetime module is used to validate dates entered by the user.

The application stores each expense as a tuple containing:

(category, amount, date)

For example:

("Food", 150.0, "28-09-2026")

All expenses are maintained inside a list.

⸻

6. Input Validation

Input validation is an important part of the application because incorrect input can lead to inaccurate records or program errors.

Category Validation

The validate_category() function removes unnecessary spaces from the input and ensures that the category is not empty.

If the user enters an empty category, the program displays:

Category cannot be empty.

Amount Validation

The validate_amount() function converts the entered amount into a floating-point number.

The program checks that:

* The entered value is a valid number.
* The amount is greater than zero.

If an invalid value is entered, the application displays an appropriate error message.

Date Validation

The validate_date() function checks whether the entered date follows the required:

DD-MM-YYYY

format.

For example:

28-09-2026

is considered a valid format, while incorrectly formatted dates are rejected.

⸻

7. Data Storage and File Handling

One of the important aspects of this project is persistent data storage.

The application uses a file named:

expenses.json

The load_expenses() function checks whether the file exists. If it exists, the stored data is loaded using the JSON module.

If the file does not exist, the application starts with an empty expense list.

The save_expenses() function writes the current expense list into the JSON file whenever a new expense is added or an existing expense is deleted.

This approach ensures that the user’s records are not lost when the program is closed.

The JSON structure provides a simple and human-readable method of storing the data.

⸻

8. Functions Used in the Project

The project is divided into multiple functions instead of placing all the code inside one large block. This makes the program easier to understand, maintain, test, and modify.

Important functions include:

validate_category()

Validates the category entered by the user.

validate_amount()

Validates and converts the expense amount.

validate_date()

Checks whether the date follows the required format.

load_expenses()

Loads previously stored expenses from the JSON file.

save_expenses()

Saves the current expenses to the JSON file.

category_summary()

Calculates total expenditure for every category.

daily_summary()

Calculates total expenditure for every date.

highest_spending_category()

Identifies the category with the highest total spending.

total_spending()

Calculates the total amount of all expenses.

add_expense()

Collects expense information and adds a new record.

view_expenses()

Displays all recorded expenses.

search_by_category()

Searches for expenses belonging to a selected category.

show_category_summary()

Displays the category-wise spending summary.

show_daily_summary()

Displays the daily spending summary.

show_highest_category()

Displays the category with the highest expenditure.

delete_expense()

Removes a selected expense.

main()

Controls the main menu and manages the overall flow of the application.

⸻

9. Programming Concepts Used

This project demonstrates several fundamental programming concepts.

Variables and Data Types

The program uses strings for categories and dates, floating-point values for amounts, lists for storing expenses, tuples for individual expense records, and dictionaries for generating summaries.

Conditional Statements

if, elif, and else statements are used to process menu selections and validate user input.

Loops

A while loop continuously displays the main menu until the user chooses the Exit option.

for loops are used to process expense records and generate summaries.

Functions

The program is divided into separate functions, with each function responsible for a particular task.

Exception Handling

try and except blocks are used to handle invalid amounts, invalid dates, invalid menu inputs, and file-related problems.

File Handling

The program uses file operations to read and write the JSON data file.

Dictionaries

Dictionaries are used for category-wise and daily spending calculations.

List Operations

Lists are used to maintain the collection of expenses. Operations such as append() and pop() are used to add and remove records.

⸻

10. Program Workflow

The general workflow of the application is:

Start
  |
  v
Load Existing Expenses
  |
  v
Display Main Menu
  |
  +----> Add Expense
  |
  +----> View Expenses
  |
  +----> Search by Category
  |
  +----> Category Summary
  |
  +----> Daily Summary
  |
  +----> Highest Spending Category
  |
  +----> Delete Expense
  |
  +----> Total Spending
  |
  +----> Exit
  |
  v
End

When the program starts, it first loads any previously saved expenses. The main menu is then displayed. The user selects an operation, and the corresponding function is executed. After completing the operation, the program returns to the main menu.

The program continues this process until the user selects option 9.

⸻

11. Error Handling

Error handling is implemented to make the application more reliable and user-friendly.

Examples include:

* Empty category input.
* Non-numeric amount.
* Zero or negative amount.
* Incorrect date format.
* Invalid expense number during deletion.
* Invalid menu selection.
* Missing JSON file.
* Invalid or corrupted JSON data.

Instead of terminating unexpectedly, the application displays an appropriate error message and allows the user to continue using the program.

For example:

Error: Amount must be greater than zero.

This improves the overall usability of the application.

⸻

12. Advantages of the Project

The Smart Daily Expense Tracker provides several advantages:

1. It is simple and easy to operate.
2. It does not require an external database.
3. Expense information is stored permanently using a JSON file.
4. It reduces manual calculations.
5. It provides both category-wise and date-wise summaries.
6. It supports searching and deleting expense records.
7. It validates user input.
8. It uses modular functions, making the program easier to maintain.
9. It demonstrates practical applications of basic Python programming concepts.
10. It can be extended with additional features in the future.

⸻

13. Limitations

Although the application provides several useful features, it currently has some limitations.

* It is a command-line application and does not have a graphical user interface.
* The data is stored locally in a JSON file.
* It does not provide user login or authentication.
* It does not generate graphical charts.
* It does not provide automatic monthly or yearly reports.
* It does not support cloud synchronization.
* It does not automatically detect recurring expenses.
* It does not include a predefined category system.

These limitations also provide opportunities for future improvements.

⸻

14. Future Enhancements

The project can be further improved by adding additional features.

Graphical User Interface

A GUI can be developed using libraries such as Tkinter or other Python frameworks to make the application more visually interactive.

Monthly and Yearly Reports

The system can be extended to generate monthly and yearly expenditure reports.

Data Visualization

Charts and graphs can be added to display spending patterns visually.

For example:

* Pie charts for category distribution.
* Bar charts for daily spending.
* Line charts for monthly spending trends.

Budget Management

Users could set a monthly budget and receive warnings when their expenditure approaches or exceeds the budget.

Export Functionality

Expense records could be exported to CSV, Excel, or PDF files.

Database Integration

Instead of JSON storage, a database such as SQLite could be used for handling a larger number of records.

User Authentication

A login system could be added so that multiple users can maintain separate expense records.

Advanced Search

Future versions could allow users to search expenses by date range, amount range, or multiple categories.

⸻

15. Conclusion

The Smart Daily Expense Tracker is a practical Python application designed to simplify the process of recording and analyzing daily expenses. The project demonstrates how fundamental programming concepts can be combined to solve a real-world problem.

The application provides essential expense management operations such as adding, viewing, searching, summarizing, deleting, and calculating expenses. It also includes input validation and exception handling to improve reliability. The use of JSON file storage allows expense information to remain available between different executions of the program.

Through this project, concepts such as functions, loops, conditional statements, lists, tuples, dictionaries, exception handling, file handling, JSON processing, and input validation are applied in a practical scenario.

The project can serve as a foundation for developing a more advanced personal finance management system in the future. With the addition of a graphical interface, database support, data visualization, budgeting features, and report generation, the application can be expanded into a more comprehensive expense management solution.

Overall, the Smart Daily Expense Tracker demonstrates the practical use of Python programming to create a structured, functional, and maintainable solution for everyday expense management.