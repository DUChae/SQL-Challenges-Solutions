
SELECT D.name AS Department <br/>

,E.name AS Employee
<br/>
,DHS.Max_salary AS Salary
<br/>
FROM Employee AS E
<br/>
INNER JOIN
<br/>
(SELECT departmentId,Max(Salary) AS Max_salary
<br/>
FROM Employee
<br/>
GROUP BY DepartmentId) AS DHS
<br/>
ON E.DepartmentId =DHS.DepartmentId
<br/>
AND E.Salary=DHS.Max_salary
<br/>
INNER JOIN Department AS D ON E.DepartmentId=D.id