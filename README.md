# Library App

## Description
The Library App is a simple library management system designed to manage books, patrons, and loans. It provides functionality for searching patrons, managing loans, and interacting with a JSON-based data storage system. The application is built using .NET 8.0 and follows a modular architecture.

## Project Structure
Library App/ ├── AccelerateDevGitHubCopilot.sln ├── README.md ├── src/ │ ├── Library.ApplicationCore/ │ │ ├── Library.ApplicationCore.csproj │ │ ├── Entities/ │ │ ├── Enums/ │ │ ├── Interfaces/ │ │ ├── Services/ │ ├── Library.Console/ │ │ ├── Library.Console.csproj │ │ ├── appSettings.json │ │ ├── CommonActions.cs │ │ ├── ConsoleApp.cs │ │ ├── ConsoleState.cs │ │ ├── Program.cs │ │ ├── Json/ │ │ │ ├── Authors.json │ │ │ ├── Books.json │ │ │ ├── BookItems.json │ │ │ ├── Loans.json │ │ │ ├── Patrons.json │ ├── Library.Infrastructure/ │ ├── Library.Infrastructure.csproj │ ├── Data/ │ ├── JsonData.cs │ ├── JsonLoanRepository.cs │ ├── JsonPatronRepository.cs ├── tests/ ├── UnitTests/ ├── LoanFactory.cs ├── PatronFactory.cs ├── UnitTests.csproj


## Key Classes and Interfaces

### **Core Classes**
- **`Library.ApplicationCore.Entities`**
  - Contains the core entities such as `Author`, `Book`, `BookItem`, `Loan`, and `Patron`.
- **`Library.ApplicationCore.Enums`**
  - Includes enumerations like `ConsoleState` for managing application states.
- **`Library.ApplicationCore.Interfaces`**
  - Defines interfaces such as `ILoanRepository`, `IPatronRepository`, `ILoanService`, and `IPatronService`.

### **Infrastructure**
- **`JsonData`**
  - Handles loading, saving, and populating data from JSON files.
- **`JsonLoanRepository`**
  - Implements `ILoanRepository` for managing loan data.
- **`JsonPatronRepository`**
  - Implements `IPatronRepository` for managing patron data.

### **Console Application**
- **`ConsoleApp`**
  - The main entry point for the application, managing user interactions and application state.
- **`Program.cs`**
  - Configures dependency injection and starts the application.

## Usage

### Prerequisites
- .NET 8.0 SDK installed on your machine.

### Running the Application
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd Library App

   2. Restore dependencies:
   ```bash
   dotnet restore