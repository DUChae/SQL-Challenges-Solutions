-- total earning= salary * months <br/>
-- maximum total earning for all employees <br/>
SELECT MAX(salary*months) , COUNT(*) <br/>
FROM employee <br/>
GROUP BY salary*months <br/>
ORDER BY salary*months DESC <br/>
LIMIT 1 <br/>


* * *
With using SubQuery <br/>

SELECT Salary*months AS Earn <br/>
            ,  COUNT(*)  <br/>
FROM Employee <br/>
WHERE (Salary*months) = (SELECT MAX(salary*months) FROM Employee) <br/>
GROUP BY Earn <br/>