SELECT P.firstName
<br/>
,P.lastName
<br/>
,A.city
<br/>
,A.state
<br/>
FROM Person P
<br/>
LEFT JOIN Address A ON P.personId=A.personId