# Library App

## Description

Library App is a modular application designed to manage library operations such as book loans, patron management, and inventory tracking. It is built using .NET and follows a clean architecture approach to ensure scalability and maintainability. The application uses JSON files for data persistence, making it easy to set up and run without requiring a database.

## Project Structure

- `AccelerateDevGHCopilot.sln` - Solution file for the project.
- `src/`
  - `Library.ApplicationCore/`
    - `Entities/` - Contains core domain entities.
    - `Enums/` - Defines enumerations used across the application.
    - `Interfaces/` - Declares interfaces for core abstractions.
    - `Services/` - Implements business logic and domain services.
    - `Library.ApplicationCore.csproj` - Project file for the Application Core.
  - `Library.Console/`
    - `appSettings.json` - Configuration file for the console application.
    - `CommonActions.cs` - Contains reusable actions for the console app.
    - `ConsoleApp.cs` - Main application logic for the console interface.
    - `ConsoleState.cs` - Manages the state of the console application.
    - `Program.cs` - Entry point for the console application.
    - `Json/` - Contains JSON data files for library records.
    - `Library.Console.csproj` - Project file for the Console application.
  - `Library.Infrastructure/`
    - `Data/` - Contains data access implementations.
    - `JsonData.cs` - Manages JSON file operations and data loading.
    - `JsonPatronRepository.cs` - Repository implementation for patron data access.
    - `JsonLoanRepository.cs` - Repository implementation for loan data access.
    - `Library.Infrastructure.csproj` - Project file for the Infrastructure layer.
- `tests/`
  - `UnitTests/`
    - `LoanFactory.cs` - Factory for creating test data related to loans.
    - `PatronFactory.cs` - Factory for creating test data related to patrons.
    - `ApplicationCore/` - Contains unit tests for the Application Core.
    - `UnitTests.csproj` - Project file for unit tests.

## Key Classes and Interfaces

- **Entities**
  - `Book` - Represents a book in the library.
  - `BookItem` - Represents a physical instance of a book.
  - `Patron` - Represents a library patron.
  - `Loan` - Represents a loan transaction.
  - `Author` - Represents an author.

- **Interfaces**
  - `IPatronRepository` - Interface for patron-related data operations.
  - `ILoanRepository` - Interface for loan-related data operations.
  - `IPatronService` - Interface for patron business logic operations.
  - `ILoanService` - Interface for loan business logic operations.

- **Services**
  - `PatronService` - Implements patron-related business logic.
  - `LoanService` - Implements loan-related business logic.
  - `NotificationService` - Handles notifications for overdue loans.

- **Data Access**
  - `JsonData` - Central data management class that loads and persists data to JSON files.
  - `JsonPatronRepository` - Repository for patron data access operations.
  - `JsonLoanRepository` - Repository for loan data access operations.

## Usage

1. Clone the repository:

   ```bash
   git clone <repository-url>