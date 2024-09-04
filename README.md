# Loan-lending-system

# Loan Lending System

## Overview

The Loan Lending System is an Angular application designed to manage loan details for users. The system supports viewing loan types, adding and editing user loan records, and displaying loan details. The application utilizes simple interest formulas and includes comprehensive validation and user interface design.

## Features

1. **Loan Types List**: Displays a scrollable list of predefined loan types in a simple table.
2. **Lend Loan Form**: Captures user and loan details, calculates simple interest, and saves or cancels loan entries.
3. **User Loan List**: Shows all users with their loan details in a table, with formatted display for dates and loan types.
4. **Detail View**: Displays loan details in a read-only format with options to delete or go back.
5. **Edit User Loan**: Allows editing of existing loan records with validation and updates.

## Screens

### Screen 1: Loan Types List

- **Layout**:
  - Displays a scrollable list of loan types in a simple table format.
  - Default loan types include: Personal Loans, Home Loans, Student Loans, Auto Loans.
  - The list is not editable or extendable.
- **Design**:
  - The table should be styled using HTML and CSS without grid lines.

### Screen 2: Lend Loan Form

- **Sections**:
  1. **User Detail**:
     - **Full Name**: Mandatory field, character validation.
     - **DOB**: Date of Birth, format `dd-mm-yyyy`, mandatory field.
     - **Comment**: Optional textarea for comments.
     - **Mobile Number**: 10-digit mandatory field.
  2. **Loan Type**:
     - Drop-down to select loan type from the list shown in Screen 1.
     - The first option in the drop-down should be "Select loan type" with a blank value.
  3. **Loan Detail**:
     - **Principal Amount (P)**: Positive integer or decimal, mandatory.
     - **Rate (R)**: Positive integer or decimal, mandatory.
     - **Time in Months (T)**: Positive integer, mandatory.
     - Read-only fields display the calculated Simple Interest (SI) and Total Amount (A).
- **Buttons**:
  - **Cancel**: Aborts operation and redirects to the user loan listing screen.
  - **Calculate**: Processes the loan details to calculate and display SI and A.
  - **Save**: Saves the loan details and redirects to the user loan listing screen.
- **Validation**:
  - Detailed validation for all fields with error messages and mandatory field indicators.

### Screen 3: User Loan List

- **Layout**:
  - Displays a table with user loan details.
  - **Date of Birth** and **Loan Type** columns use custom pipes:
    - **`dateFormat` Pipe**: Formats date from `dd-mm-yyyy` to `dd Month, YYYY` (e.g., 21-09-2022 to 21 Sep, 2022).
    - **`formatText` Pipe**: Transforms loan type to title case (e.g., "personal loan" to "Personal Loan").
  - **Calculation**: Displays the loan formula with exact values for P, R, and T.

### Screen 4: Detail View

- **Layout**:
  - Same as the lend loan form but pre-filled with user loan data and all fields in read-only mode.
- **Buttons**:
  - **Back**: Returns to the user loan listing screen.
  - **Delete** (Red Button): Deletes the entry and redirects to the user loan listing screen.

### Screen 5: Edit User Loan

- **Layout**:
  - Same as the lend loan form but pre-filled with existing data for editing.
- **Buttons**:
  - **Back**: Returns to the user loan listing screen.
  - **Update** (Red Button): Updates the loan record and redirects to the user loan listing screen.

## Installation

To set up the project locally, follow these steps:

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/yourusername/loan-lending-system.git
    ```

2. **Navigate to Project Directory**:
    ```bash
    cd loan-lending-system
    ```

3. **Install Dependencies**:
    ```bash
    npm install
    ```

4. **Run the Application**:
    ```bash
    ng serve
    ```

5. **Open in Browser**:
    Navigate to `http://localhost:4200` to view the application.

## Usage

- **Navigate between screens** using the menu.
- **Add and edit loan records** with validation and calculation features.
- **View and manage user loan details** in a formatted table.

## Contributing

Contributions are welcome! Please submit issues and pull requests. For significant changes, open an issue to discuss proposed modifications.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Angular framework
- Bootstrap for UI components
- Custom date and text formatting pipes


