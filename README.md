# Lib repository
By leveraging modern technologies and best practices, the proposed solution aims to create a robust and user-friendly platform that meets the diverse needs of libraries and patrons. At its core, the system enables users to search for books, facilitating easy access to the library's collection. Functions for issuing and returning books streamline transactions, ensuring a smooth borrowing experience for patrons.

-> Fines management is integrated into the system, allowing users to check for any fines associated with overdue books, thus promoting accountability and timely returns. Librarian privileges include accessing member information, tracking books issued by specific students, and managing membership by adding or removing students as needed. Additionally, librarians can oversee the library's inventory by adding, deleting, or updating book records and adjusting availability statuses

-> The system's administrative dashboard provides comprehensive tools for managing member and book records. Admins can view, update, or delete member and book records, ensuring data accuracy and system integrity. Modules such as admin login, book search, book and member management, and book issuance further enhance the system's functionality, catering to diverse user needs.

-> Technologically, the system leverages a robust stack comprising HTML, CSS, JavaScript, PHP, and MySQL. HTML, CSS, and JavaScript are utilized for creating an intuitive and responsive user interface, while PHP serves as the server-side scripting language for processing user requests and interacting with the database. 
-> MySQL functions as the database management system, storing and managing data related to books, members, transactions, and fines.

In summary, the library management system offers a comprehensive solution for efficiently managing library resources and operations. With its user-friendly interface, extensive librarian capabilities, administrative tools, and robust technology stack, the system empowers libraries to streamline their processes, enhance user experiences, and maintain accurate records.

1.2	Entity And Relationships
1.2.1 Entities Used
• Books:
Attributes: book code, book name, subject code, author, price, status (available, issued, lost, damaged), date issued, and date return                                       
• Members:
Attributes: member ID, name, address, date of expiry of membership, and status of book issues (which books they have currently borrowed and their respective due dates).
• Transactions:
Attributes: book code, member ID, date borrowed, date returned (optional, indicating if the book has been returned).

# Relationships
- Books are associated with a one-to-many relationship with members, indicating that a single book can be issued to multiple members over time.
- Conversely, members have a many-to-many relationship with books, allowing them to borrow multiple books from the library's collection.
- Transactions serve to track the borrowing and returning of books by members, creating a record of each interaction between a member and a book.
- Each transaction includes details such as the book borrowed, the member involved, the date of borrowing, and the due date for return.
- When a member borrows a book, a new transaction record is created, indicating the start of the borrowing period.
- Upon returning the book, the corresponding transaction record is updated to reflect the return date, effectively closing the borrowing transaction.
- Transactions provide a comprehensive history of book movements within the library, facilitating inventory management and fine calculation.
- The relationships between books, members, and transactions form the backbone of the library management system, enabling efficient tracking and management of library 
  resources and patron interactions.
  
  When a member borrows a book, a new transaction record is created in the transactions table.
  This transaction record includes a reference to both the member and the book involved in the borrowing transaction.
  The transaction record also stores additional details such as the date of borrowing and the due date for return.






