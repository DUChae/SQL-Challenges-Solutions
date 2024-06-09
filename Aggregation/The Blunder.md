SELECT CEIL(AVG(salary) - AVG(REPLACE(salary,0,''))) <br/>
FROM Employees
