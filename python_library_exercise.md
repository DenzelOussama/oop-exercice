# Python Programming Exam
**Time Limit: 3 hours**  
**Total Points: 100**
*ignore this message its just me trying git,this message will be added,commited and pushed in couple minutes*
## Instructions
- Read all questions carefully before starting
- Code must be properly commented
- Test your code before submitting
- Handle edge cases and errors appropriately

---

## Question 1: Book Class Implementation (15 points)

Create a `Book` class with the following requirements:

**a)** Initialize the class with these attributes: `isbn`, `title`, `author`, `genre`, `publication_year`, and `is_available` (default True). **(5 points)**

**b)** Implement a `__str__` method that returns: "Title by Author (Year) - Available/Borrowed". **(3 points)**

**c)** Create a method `borrow()` that sets `is_available` to False and returns "Book borrowed successfully" or "Book already borrowed". **(4 points)**

**d)** Create a method `return_book()` that sets `is_available` to True. **(3 points)**

---

## Question 2: Member Class Implementation (20 points)

Create a `Member` class with the following specifications:

**a)** Initialize with `member_id`, `name`, `email`, and an empty list called `borrowed_books`. **(5 points)**

**b)** Create a method `add_borrowed_book(isbn)` that adds the ISBN to the borrowed_books list only if the member has fewer than 3 borrowed books. Return appropriate success/failure messages. **(8 points)**

**c)** Implement `remove_borrowed_book(isbn)` that removes the ISBN from borrowed_books if it exists. **(4 points)**

**d)** Create a property method `can_borrow` that returns True if the member can borrow more books (less than 3). **(3 points)**

---

## Question 3: Library Management System (25 points)

Create a `Library` class that manages books and members:

**a)** Initialize with `name` and two empty dictionaries: `books` (ISBN as key) and `members` (member_id as key). **(5 points)**

**b)** Implement `add_book(book_object)` that adds the book to the books dictionary. Handle the case where ISBN already exists. **(5 points)**

**c)** Implement `register_member(member_object)` that adds the member to members dictionary. Prevent duplicate member_ids. **(5 points)**

**d)** Create `borrow_book(member_id, isbn)` that:
- Checks if member and book exist
- Verifies book is available and member can borrow
- Updates both book and member objects
- Returns appropriate success/error messages
**(10 points)**

---

## Question 4: Search and Filter Functions (15 points)

Add these methods to your Library class:

**a)** `find_books_by_author(author_name)` - Returns a list of all books by the given author (case-insensitive). **(5 points)**

**b)** `get_available_books()` - Returns a list of all available books. **(5 points)**

**c)** `get_member_borrowed_books(member_id)` - Returns a list of Book objects currently borrowed by the member. **(5 points)**

---

## Question 5: File Operations and Error Handling (15 points)

**a)** Create a custom exception class `LibraryError` with an appropriate error message. **(3 points)**

**b)** Add a method `save_library_data(filename)` to the Library class that saves all books and members to a text file in a readable format. Handle file errors appropriately. **(6 points)**

**c)** Modify your `borrow_book` method to raise `LibraryError` with specific messages for different error conditions (member not found, book not found, book not available, member can't borrow). **(6 points)**

---

## Question 6: Data Analysis and Reporting (10 points)

Create a method `generate_report()` in your Library class that returns a dictionary containing:

**a)** Total number of books and members **(2 points)**

**b)** Number of available vs borrowed books **(3 points)**

**c)** Most popular author (author with most books in library) **(3 points)**

**d)** List of members who haven't borrowed any books **(2 points)**

---

## Bonus Question: Advanced Implementation (10 extra points)

**a)** Create a `PremiumMember` class that inherits from `Member` and can borrow up to 5 books instead of 3. **(5 points)**

**b)** Add a method `calculate_late_fees(days_late)` to the Member class that calculates fees at $2 per day for regular members and $1 per day for premium members. **(5 points)**

---

## Testing Section (Required)

Write a main function that demonstrates:
1. Creating a library with at least 5 books
2. Registering at least 3 members
3. Performing borrowing operations (both successful and failed)
4. Searching for books by author
5. Generating and printing a library report
6. Demonstrating error handling

**Example expected output:**
```
=== Library System Test ===
Added book: Python Programming by John Smith (2020)
Registered member: Alice Johnson (ID: M001)
Alice borrowed: Python Programming - Success
Alice tried to borrow unavailable book - Error: Book not available
=== Library Report ===
Total Books: 5, Total Members: 3
Available: 2, Borrowed: 3
Most Popular Author: John Smith
```

---

## Grading Criteria:
- **Functionality (60%)**: Code works as specified
- **Code Quality (20%)**: Clean, readable, well-commented code
- **Error Handling (10%)**: Proper exception handling
- **Testing (10%)**: Comprehensive test cases in main function

**Good luck!**
