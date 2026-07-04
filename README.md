# Employee Management System API

A simple FastAPI-based REST API for managing employee records with CRUD operations.

## 📋 Features

- **Create Employee**: Add new employees to the system
- **Read Employees**: Retrieve all employees or a specific employee by ID
- **Update Employee**: Modify employee details
- **Delete Employee**: Remove employees from the system
- **Department Classification**: Support for HR, IT, Finance, and Marketing departments
- **Data Validation**: Built-in validation using Pydantic models

## 🛠️ Technology Stack

- **FastAPI** - Modern web framework for building APIs with Python
- **Pydantic** - Data validation and serialization
- **Python 3.7+** - Programming language

## 📦 Installation

1. Clone the repository:
```bash
git clone https://github.com/samarthrana027/Employeemanage_fastapi.git
cd Employeemanage_fastapi
```

2. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install fastapi uvicorn
```

## 🚀 Running the Application

Start the FastAPI server:
```bash
uvicorn employeemanage_fastapi:app --reload
```

The API will be available at `http://localhost:8000`

### Interactive API Documentation
- **Swagger UI**: http://localhost:8000/docs
- **ReDoc**: http://localhost:8000/redoc

## 📚 API Endpoints

### Create Employee
```
POST /employees/
Content-Type: application/json

{
  "id": 1,
  "name": "John Doe",
  "age": 30,
  "department": "IT",
  "salary": 75000,
  "is_active": true
}
```

### Get All Employees
```
GET /employees/
```

### Get Single Employee
```
GET /employees/{employee_id}
```

### Update Employee
```
PUT /employees/{employee_id}
Content-Type: application/json

{
  "id": 1,
  "name": "Jane Doe",
  "age": 31,
  "department": "HR",
  "salary": 80000,
  "is_active": true
}
```

### Delete Employee
```
DELETE /employees/{employee_id}
```

## 📋 Employee Model

```python
{
  "id": int,              # Unique employee identifier
  "name": str,            # Employee full name
  "age": int,             # Employee age
  "department": str,      # Department (HR, IT, Finance, Marketing)
  "salary": float,        # Annual salary
  "is_active": bool       # Active status (default: true)
}
```

## 🏢 Supported Departments

- **HR** - Human Resources
- **IT** - Information Technology
- **Finance** - Finance Department
- **Marketing** - Marketing Department

## 📝 Error Handling

The API provides appropriate HTTP status codes:

- **400 Bad Request**: Employee ID already exists
- **404 Not Found**: Employee not found
- **422 Unprocessable Entity**: Invalid data format

## 💾 Data Storage

Currently, the application uses an in-memory list for data storage. Data will be lost when the server restarts.

**Note**: For production use, integrate with a database (PostgreSQL, MongoDB, etc.)

## 🔧 Future Enhancements

- Database integration (PostgreSQL/MongoDB)
- User authentication and authorization
- Employee search and filtering
- Pagination for large datasets
- Logging and monitoring
- Unit and integration tests

## 📄 License

This project is open source and available under the MIT License.

## 👤 Author

**Samarth Rana** - samarthrana027

## 📧 Support

For issues or questions, please open an issue in the repository.
