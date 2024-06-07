SELECT DISTINCT L1.num AS ConsecutiveNums <br/>

FROM Logs AS L1 <br/>

INNER JOIN Logs AS L2 ON L1.id+1=L2.id
<br/>
INNER JOIN Logs AS L3 on L1.id+2 = L3.id
<br/>
WHERE L1.num=L2.num AND L1.num=L3.num