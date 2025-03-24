# Product API (CRUD) - .NET Core

This is a simple **CRUD API** for managing products, built with **.NET Core** and **Entity Framework Core**.

## 🛠️ Requirements
- .NET 6 or later
- SQL Server
- Postman or any API testing tool

## 📦 Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/your-repo.git
   cd your-repo
   ```

## ⚙️ Configuration

1. **Rename the configuration file**:
    ```bash
    cp appsettings.json.example appsettings.json
    ```

2. **Update your database credentials:**

Open the `appsettings.json` file and modify the `ConnectionStrings` section:

```json
"ConnectionStrings": {
  "DefaultConnection": "Server=YOUR_SERVER;Database=YOUR_DB;User Id=YOUR_USER;Password=YOUR_PASSWORD;TrustServerCertificate=True;"
}
```

✅ **Replace the placeholders:**
- `YOUR_SERVER`: Your SQL Server instance (e.g., localhost, DESKTOP-XXXXXX, etc.)
- `YOUR_DB`: The database name (e.g., ProductDb)
- `YOUR_USER`: Your SQL Server username
- `YOUR_PASSWORD`: Your SQL Server password

3. **Ensure the Entity Framework Core tools are installed**

If not already installed, add the tools package:

```bash
dotnet add package Microsoft.EntityFrameworkCore.Tools
```

4. **Generate the initial migration**

This command creates the files needed to build the database structure (tables, relationships, etc.) from the `Product` model:

```bash
dotnet ef migrations add InitialCreate
```

This will generate a `Migrations/` folder with the scripts to create the `Products` table.

5. **Apply the migration to the database**

This command runs the scripts and physically creates the database in SQL Server:

```bash
dotnet ef database update
```

## ▶️ Execution

Run the API with the following command:

```bash
   dotnet run
```

Access the Swagger interface to test the endpoints:

[http://localhost:5278/swagger/](http://localhost:5278/swagger/)

