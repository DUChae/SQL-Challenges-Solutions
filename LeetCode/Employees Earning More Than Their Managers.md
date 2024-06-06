SELECT Employee.name AS Employee <br/>
 
FROM Employee <br/>

INNER JOIN Employee AS manager ON Employee.managerid = Manager.Id
<br/>
WHERE Employee.salary>Manager.salary