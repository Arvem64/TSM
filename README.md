Training Sessions Manager Prototype

*****************************************
Technologies Used:
 - .NET 8.0 Framework      
 - C#, XAML      
 - Entity Framework 6 (EF 6)     
 - MVVM Pattern      
 - Unit of Work & Repositories      
 - Two-Way Data Binding

Overview
The Training Sessions Manager App (Prototype) is designed to manage training sessions efficiently. Built with .NET 8.0, C#, and XAML, the application integrates Entity Framework 6 (EF 6) for data access. It implements key design patterns such as MVVM (Model-View-ViewModel) and Unit of Work, ensuring a clean architecture that promotes scalability and maintainability. The application provides a dynamic and responsive user experience by leveraging two-way data binding to synchronize the ViewModel and View.
Key Features & Architecture

1. Unit of Work & IRepositories
 - Unit of Work Pattern: The app utilizes the Unit of Work (UoW) pattern to manage transactions and interactions across multiple repositories, ensuring consistency during data access and modifications. This design helps in reducing repetitive code and promoting cleaner code management.
 - Repositories: Custom IRepositories provide abstraction for CRUD operations with the database, allowing efficient querying and data manipulation through Entity Framework 6 (EF 6).

2. Data Binding (Two-Way Binding with MVVM)
  - MVVM Pattern: The app follows the MVVM (Model-View-ViewModel) pattern, which helps in abstracting the UI (View) from the business logic (ViewModel), making the application easier to maintain and test.
  - Two-Way Data Binding: The application implements two-way data binding to ensure dynamic and synchronized updates between the ViewModel and the View. Changes made in the UI are immediately reflected in the ViewModel, and updates in the ViewModel are displayed in the UI.
The controls are populated with lists from the ViewModels, and the selected item are bound to properties in the ViewModels for real-time updates.

3. DbContext Configuration & Entity Framework 6 (EF 6)
DbContext: The app uses Entity Framework 6 (EF 6) as the ORM (Object-Relational Mapping) tool to facilitate interaction with the underlying SQL database. The DbContext manages the database entities and handles CRUD operations for them. The configuration is based on the Fluent API in the OnModelCreating method of the DbContext and the ObservableCollection for managing data collections with automatic UI updates.

Achievements
  - Implemented the Unit of Work pattern to manage database operations, ensuring data consistency and ease of transaction management.
  - Utilized MVVM architecture to promote abstraction of concerns and improved testability, enhancing long-term maintainability.
  - Leveraged two-way data binding between XAML controls (such as ComboBox and DataGridView) and the ViewModel, ensuring that the UI reflects updates in real-time.
  - Configured Entity Framework 6 (EF 6) for database interaction, enabling efficient data management and support for linking the entities.
