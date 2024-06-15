SELECT class
<br/>
FROM Courses
<br/>
GROUP BY class
<br/>
HAVING COUNT(*)>=5