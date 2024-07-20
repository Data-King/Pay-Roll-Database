---- CREATE TABLES 
---- Employee


CREATE TABLE Employee(  
    Employee_id INT(6),
    First_name VARCHAR(25),
    Last_name VARCHAR(25),
    Hire_date DATE,
    City VARCHAR(25),
    State VARCHAR(25),
    CONSTRAINT Employee_pk PRIMARY KEY(Employee_id)
);

---- Department

CREATE TABLE Department(
    Department_id INT,
    Department_name VARCHAR(30),
    CONSTRAINT Department_pk PRIMARY KEY(Department_id)
);

---- Salary 
CREATE TABLE Salary(
    Salary_id INT,
    Gross_salary INT,
    Hourly_pay INT,
    State_tax INT,
    Federal_tax INT,
    Account_id INT,
    CONSTRAINT Salary_pk PRIMARY KEY(Salary_id),
    Foreign Key (Account_id) REFERENCES Account(id)
    );

---- Department Project Bridge
CREATE TABLE DepartmentProject(
    Department_id INT,
    Project_id INT,
    CONSTRAINT DeptProject_pk PRIMARY KEY(Department_id,Project_id),
    Foreign Key (Department_id) REFERENCES Department(id),
    Foreign Key (Project_id) REFERENCES Department(id)
);
---- Project
CREATE TABLE Project(
    Project_id INT,
    Project_name VARCHAR(50),
    Project_description VARCHAR(50),
    CONSTRAINT Project_pk PRIMARY KEY(Project_id)
);

---- Account Details
CREATE TABLE AccountDetails(
    Account_id INT,
    Bank_name VARCHAR(50),
    Account_name VARCHAR(50),
    Employee_id INT,
    CONSTRAINT Account_pk PRIMARY KEY(Account_id),
    Foreign Key (Employee_id) REFERENCES Employee(id)
);


---- Education
CREATE TABLE Education(
    Education_id INT,
    Employee_id INT,
    Degree VARCHAR(30),
    Grad_year INT(4),
    CONSTRAINT Location_pk PRIMARY KEY(Education_id),
    Foreign Key (Employee_id) REFERENCES Employee(id)
);

--- Leave
CREATE TABLE Leave(
    Leave_id INT,
    Employee_id INT,
    Leave_date DATE,
    CONSTRAINT Leave_pk PRIMARY KEY(Leave_id),
    Foreign Key (Employee_id) REFERENCES Employee(id)
);

---- Employee Attendance Bridge
CREATE TABLE Employee_Attendance(
    Employee_id INT,
    Attendance_id INT,
    CONSTRAINT Department_Project_pk PRIMARY KEY(Employee_id,Attendance_id),
    Foreign Key (Employee_id) REFERENCES Employee(id),
    Foreign Key (Attendance_id) REFERENCES Attendance(id)
);



---- Attendance
CREATE TABLE Attendance(
    Attendance_id INT,
    Hours_worked INT,
    CONSTRAINT Attendance_pk PRIMARY KEY(Attendance_id)
);




---- Work Location
CREATE TABLE Work_Location(
    Location_id INT,
    Location VARCHAR(25),
    Num_of_Employees INT,
    City VARCHAR(25),
    State VARCHAR(25),
    CONSTRAINT Loc_pk PRIMARY KEY(Location_id)
);


------------------------------------------------------------------------------------------------------
