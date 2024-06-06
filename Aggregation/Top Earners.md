-- total earning= salary * months <br/>
-- maximum total earning for all employees <br/>
SELECT MAX(salary*months) , COUNT(*) <br/>
FROM employee <br/>
GROUP BY salary*months <br/>
ORDER BY salary*months DESC <br/>
LIMIT 1
