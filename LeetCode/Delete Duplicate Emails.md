DELETE p1 <br/>

FROM Person p1
<br/>
INNER JOIN Person p2 ON p1.email=p2.email
<br/>
WHERE p1.id>p2.id