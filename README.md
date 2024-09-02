# Library Management System

This SQL project covers everything from table creation and data insertion to queries, updates, and deletions, allowing efficient management of a library.

## Database Structure

- **Authors**: Contains information about the book authors.
- **Books**: Contains information about the books, including the author, year of publication, and genre.
- **Loans**: Records information about book loans, including the loan date, return date, and the user’s name.

## Created Tables

1. **Authors**
    - `AuthorID` (INT, PK, Auto Increment)
    - `Name` (VARCHAR(100), NOT NULL)
    - `Nationality` (VARCHAR(100))

2. **Books**
    - `BookID` (INT, PK, Auto Increment)
    - `Title` (VARCHAR(255), NOT NULL)
    - `AuthorID` (INT, FK, REFERENCES Authors)
    - `PublicationYear` (YEAR)
    - `Genre` (VARCHAR(50))

3. **Loans**
    - `LoanID` (INT, PK, Auto Increment)
    - `BookID` (INT, FK, REFERENCES Books)
    - `LoanDate` (DATE, NOT NULL)
    - `ReturnDate` (DATE)
    - `UserName` (VARCHAR(100), NOT NULL)

## Database Operations

### Data Insertion
- Authors: Includes 5 authors of different nationalities.
- Books: Includes 10 books with different genres and publication years.
- Loans: Records 5 loans with user information and loan/return dates.

### Queries
- Selects all books with their respective authors and publication years.
- Selects loans where the return date has not been filled yet.

### Update
- Updates the return date of a specific loan.

### Deletion
- Deletes a specific loan.
- Deletes a specific book.

## How to Use

1. Create the database and tables using the provided SQL commands.
2. Insert the data into the tables using `INSERT INTO` commands.
3. Run the queries, updates, and deletions as needed.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
