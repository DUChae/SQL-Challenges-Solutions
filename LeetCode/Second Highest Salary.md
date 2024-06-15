SELECT MAX(salary) AS SecondHighestSalary
<br/>
FROM Employee
<br/>
WHERE salary < (SELECT MAX(salary)
<br/>
FROM Employee
<br/>
)