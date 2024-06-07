
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


---
With Using Window

SELECT ms.department AS Department
<br/>
,ms.name AS Employee
<br/>
,ms.salary AS Salary
<br/>
FROM
<br/>
(SELECT
<br/>
E.name
<br/>
,E.salary
<br/>
,D.name AS Department
<br/>
,MAX(salary) OVER (PARTITION BY Departmentid) AS max_salary
<br/>
FROM Employee AS E
<br/>
INNER JOIN Department AS D ON E.DepartmentId=D.id) ms
<br/>
WHERE ms.salary=ms.max_salary