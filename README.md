Training Sessions Manager App

*****************************************
Technologies Used:
 - .NET 8.0 Framework      
 - C#, XAML      
 - Entity Framework 6 (EF 6)     
 - MVVM Pattern      
 - Unit of Work & Repositories      
 - Two-Way Data Binding 

Overview :
The Training Sessions Manager App (Prototype) is designed to manage training sessions. Built with .NET 8.0, C#, and XAML, the application integrates Entity Framework 6 (EF 6) for data access. It implements key design patterns such as MVVM (Model-View-ViewModel) and Unit of Work, ensuring a clean architecture that promotes scalability and maintainability. The application provides a dynamic and responsive user experience by leveraging two-way data binding to synchronize the ViewModel and View. 

Key Features & Architecture:

1. Unit of Work & IRepositories
 - Unit of Work Pattern: The app utilizes the Unit of Work (UoW) pattern to manage transactions and interactions across multiple repositories, ensuring consistency during data access and modifications. This scheme helps in reducing repetitive code and promoting cleaner code management.
 - Repositories: Custom IRepositories provide abstraction for CRUD operations with the database, allowing efficient querying and data manipulation through Entity Framework 6 (EF 6).

2. Data Binding (Two-Way Binding with MVVM) for a quick implementation serving just test purposes
  - MVVM Pattern: The app follows the MVVM (Model-View-ViewModel) pattern, which helps in abstracting the UI (View) from the business logic (ViewModel), making the application easier to maintain and test.
  - Two-Way Data Binding: The application implements two-way data binding to ensure dynamic and synchronized updates between the ViewModel and the View. Changes made in the UI are immediately reflected in the ViewModel, and updates in the ViewModel are displayed in the UI.
The controls are populated with lists from the ViewModels, and the selected items are bound to properties in the ViewModels for real-time updates.

3. DbContext Configuration & Entity Framework 6 (EF 6)
DbContext: The app uses Entity Framework 6 (EF 6) as the ORM (Object-Relational Mapping) tool to facilitate interaction with the underlying SQL database. The DbContext manages the database entities and handles CRUD operations for them. The configuration is based on the Fluent API in the OnModelCreating method of the DbContext and the ObservableCollection for managing data collections with automatic UI updates.

Achievements
  - Implemented the Unit of Work pattern to manage database operations, ensuring data consistency and ease of transaction management.
  - Utilized MVVM architecture to promote abstraction of concerns and improved testability, enhancing long-term maintainability.
  - Leveraged two-way data binding between XAML controls (such as ComboBox and DataGridView) and the ViewModel, ensuring that the UI reflects updates in real-time.
  - Configured Entity Framework 6 (EF 6) for database interaction, enabling efficient data management and support for linking the entities.

The Setup is located in ~LocalFolder~\TrainingSessions\TrainingSessions\bin\Release\net8.0-windows folder.


NB : The business logic is to be customized based on one's project's fixed objectives. The goal here is to shed light on the working principle of Entity Framework and test it.

Recommendations :
- Using the ViewModel pattern throughout the implementation will enhance the code's efficiency and robustness. For instance, wrap the ObservableCollection of the ViewModel in a CollectionViewSource instead of using the Model's ObservableCollection, or simply use the ViewModel's collection. This will require modifying the DataGridViews' DataContexts of each window in the XAML code.
- Avoid directly inheriting the Model classes from the INotifyPropertyChanged interface, and instead, adopt the ViewModel approach.
- Implement and call generic methods for repetitive tasks to clean up the code and improve maintainability.
- The One-Way Data Binding approach would be a better blueprint to apply, particularly in production environments (The purpose of utilizing Two-Way Data Binding is to allow users to visualize the results in a user-friendly interface rather than using the C# console, as this model is just intended for testing).
- Add an Authentication Window as the main page (which involves modifying the StartupUri in App.xaml) and ensure the correct privileges are set for each authenticated and authorized user.
- Implementing Regex patterns to validate user input.
- Installing the BCrypt NuGet package to hash the passwords of user accounts.

TSM!
