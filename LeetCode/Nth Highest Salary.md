With using CASE WHEN  <br/>
CREATE FUNCTION getNthHighestSalary(N INT) RETURNS INT<br/>



BEGIN
<br/>
RETURN (
<br/>
SELECT CASE
<br/>
WHEN N<=0 THEN NULL
<br/>
WHEN COUNT(DISTINCT sub.salary) < N THEN NULL
<br/>
ELSE MIN(sub.salary)
<br/>
END
<br/>
FROM (
<br/>
SELECT DISTINCT Salary
<br/>
FROM Employee
<br/>
ORDER BY Salary DESC
<br/>
LIMIT N
<br/>
) sub
<br/>
);
<br/>
END;


---
With using IF
<br/>
CREATE FUNCTION getNthHighestSalary(N INT) RETURNS INT
<br/>
BEGIN
<br/>
RETURN (
<br/>
SELECT IF (N<=0
<br/>
,NULL
<br/>
,IF(COUNT(sub.salary) < N
 <br/>
,NULL
<br/>
,MIN(sub.salary) ))
<br/>
FROM (
<br/>
SELECT DISTINCT Salary
<br/>
FROM Employee
<br/>
ORDER BY Salary DESC
<br/>
LIMIT N
<br/>
) sub
<br/>
);
<br/>
END;