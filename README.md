
-- 1. Creating the Managers table
CREATE TABLE Managers (
    Manager_Id INT PRIMARY KEY,
    First_Name VARCHAR(50),
    Last_Name VARCHAR(50),
    DOB DATE,
    Age INT CHECK (Age > 0), -- Check constraint for Age
    Last_Update DATE,
    Gender VARCHAR(10),
    Department VARCHAR(50),
    Salary DECIMAL(10, 2) NOT NULL -- Making Salary NOT NULL
);

-- 2. Inserting 10 rows
INSERT INTO Managers (Manager_Id, First_Name, Last_Name, DOB, Age, Last_Update, Gender, Department, Salary)
VALUES 
    (1, 'John', 'Doe', '1980-05-15', 44, '2024-06-05', 'Male', 'HR', 35000.00),
    (2, 'Jane', 'Smith', '1975-10-20', 49, '2024-06-05', 'Female', 'IT', 40000.00),
    (3, 'Michael', 'Johnson', '1982-03-08', 42, '2024-06-05', 'Male', 'Finance', 30000.00),
    (4, 'Emily', 'Brown', '1990-12-25', 34, '2024-06-05', 'Female', 'IT', 28000.00),
    (5, 'Christopher', 'Martinez', '1978-08-12', 46, '2024-06-05', 'Male', 'HR', 32000.00),
    (6, 'Jessica', 'Taylor', '1985-06-30', 39, '2024-06-05', 'Female', 'Finance', 28000.00),
    (7, 'Daniel', 'Anderson', '1970-04-18', 54, '2024-06-05', 'Male', 'IT', 42000.00),
    (8, 'Laura', 'Wilson', '1988-09-10', 36, '2024-06-05', 'Female', 'Finance', 35000.00),
    (9, 'Matthew', 'Thomas', '1976-11-22', 48, '2024-06-05', 'Male', 'IT', 38000.00),
    (10, 'Sarah', 'Garcia', '1983-07-04', 41, '2024-06-05', 'Female', 'HR', 31000.00);

-- 3. Retrieve the name and date of birth of the manager with Manager_Id 1
SELECT First_Name, Last_Name, DOB
FROM Managers
WHERE Manager_Id = 1;

-- 4. Display records of all managers except 'Aaliya'
SELECT *
FROM Managers
WHERE First_Name != 'Aaliya';

-- 5. Display details of managers whose department is IT and earns more than 25000 per month
SELECT *
FROM Managers
WHERE Department = 'IT' AND Salary > 25000.00;

-- 6. Display details of managers whose salary is between 10000 and 35000
SELECT *
FROM Managers
WHERE Salary BETWEEN 10000.00 AND 35000.00;
