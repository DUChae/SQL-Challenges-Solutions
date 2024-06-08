 join 은 employee.departmentid=department.id
<br/>
각 부서에서 돈을 가장 많이 받는 사람 탑3
<br/><br/>
SELECT Ranked.department
<br/>
,Ranked.employee
<br/>
,Ranked.salary
<br/>
FROM
<br/>
(SELECT D.name AS Department
<br/>
,E.name AS Employee
<br/>
,E.salary
<br/>
,DENSE_RANK() OVER(PARTITION BY E.departmentid ORDER BY E.salary DESC) AS RANKING
<br/>
FROM Employee AS E
<br/>
INNER JOIN Department AS D ON E.departmentid=D.id) Ranked
<br/>
WHERE Ranked.Ranking<=3