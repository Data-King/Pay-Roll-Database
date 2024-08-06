-------------------------------------------------------------------------------------------------------------------------------
---- Concepts:

---- Number of Employees with different degrees
SELECT "Degree", count("Degree")
FROM "Education"
GROUP BY "Degree";


------- How many department projects? ------------
SELECT "DepartmentProject" ,count('DepartmentProject')
FROM "DepartmentProject"
GROUP BY "Project_id";


---- Order of Salary highest to lowest
SELECT Salary_id, Gross_salary
FROM "Salary" 
ORDER BY "Salary_id", Gross_salary ASC;

--------- Each Employee's State Tax and Federal Tax ----------

SELECT Salary_id, State_tax
FROM "Salary"
WHERE "State_tax" >=400 AND "Federal_tax" >= 1400;

----------- Number of Employees --------
SELECT count(Employee_id)
FROM "Employee";




---- List all employees
SELECT * FROM "Employee" LIMIT 10;


---- How many departments?

SELECT count(*) FROM "Department";

---- How many times has Employee 10001 has a raise?
SELECT count(*) AS numb_of_raises FROM "Salary"
WHERE "Salary_id" = 4;

---- What bank emp 40 has?
SELECT Bank_name FROM "AccountDetails"
WHERE "Account_id" = 44;



---- Column Concat -----
SELECT * ,
group_concat(First_name,'',Last_name) AS FullName
FROM "Employee"
ORDER BY FullName;




---------- Types of Functions
/* Aggregate - operate on MANY record to produce ONE value, example: Sum of salaries
Scalar - operate on EACH record Independently, example: CONCAT, it doesn't return result of concat value
*/

--------- Aggregate Functions
/*
AVG()
COUNT()
MIN()
MAX()
SUM()
*/

SELECT count(*) FROM "Employee";

SELECT min(Hours_worked) FROM "Attendance";

---- Get the higherst salary avaliable
SELECT max("Gross_salary") AS Max_Salary FROM "Salary";

---- Get the total amount of salaries paid
SELECT sum(Gross_salary) AS Total_Salary_Paid FROM "Salary";


----- Filtering Data

----- Get a list of all Employee From California
SELECT * FROM "Employee"
WHERE "State" = 'California';

----- AND OR -----------
SELECT *
FROM "Employee"mployees
WHERE (first_name = 'Georgi' AND last_name='Facello' AND hire_date='1986-06-26')
OR (first_name='Bezalel' AND last_name='Simmel');


------- NOT ---------------
----------How many employees hourly pay not 30 ------------
SELECT count("Hourly_pay") FROM "Salary"
WHERE NOT "Hourly_pay"=30;

---- How many Employee's Attendance is above 95% -----

SELECT * FROM "Employee_Attendance"
WHERE "Attendance_id" >= 95;

----- Number of Employee earning 70k and pays above 1300 in Federal Tax
SELECT count(*)
FROM "Salary"
WHERE "Gross_salary" >= 70000 AND "Federal_tax" >= 1300;



----- Whos salary is between 50k and 80k
SELECT *
FROM "Salary"
WHERE "Gross_salary" BETWEEN 50000 AND 80000;


---- Average Hourly Pay-----
SELECT avg(Hourly_pay)
FROM "Salary";



/***** 18) Logical Operators AND OR NOT *****/
/* 
Order of Operations 
FROM => WEHRE => SELECT 
*/

/***** 19) Operator Precedence ******/
/* 
(most importance to least importance)

Parentheses
Multiplication / Division
Subtraction / Addition
NOT
AND
OR

If operators have equal precedence, then the operators are evaluated directionally.
From Left to Right or Right to Left.

check Operators Precedence.png
*/

SELECT State, City, "Employee_id" FROM "Employee"
WHERE "State" = 'California' OR "City" = 'Miami';



SELECT * 
FROM "Salary"
WHERE(
    "Gross_salary" >= 80000 AND "State_tax" >= 300
    OR (
        "Hourly_pay" >= 40 AND "Federal_tax" >= 1000
    )
);



---------- Checking for NULL Values -----------
SELECT NULL=NULL;
SELECT  NULL <> NULL;


------------- IS Keyword --------------

SELECT * FROM "Department"
WHERE "Department_name" = 'Human Resources' IS FALSE;  --- meaning FALSE, but not a good way to write it


SELECT * FROM "Department"
WHERE "Department_name" = 'Data Analysis' IS NOT FALSE; ------- meaning TRUE




/******* 24) NULL Value Substituion NULL Coalesce *****/
/*
	SELECT coalesce(<column>, 'Empty') AS column_alias
	FROM <table>
	
	
	SELECT coalesce(
		<column1>,
		<column2>,
		<column3>,
		'Empty') AS combined_columns
	FROM <table>
	
Coalsece returns first NON NULL value.

*/




SELECT sum(coalesce(Hours_worked, 10))
FROM "Attendance";
