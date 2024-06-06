SELECT Today.id AS Id <br/>

FROM Weather AS Today <br/>

INNER JOIN Weather AS Yesterday ON DATE_ADD(Yesterday.recordDate,INTERVAL 1 DAY) = Today.recordDate <br/>

WHERE Today.temperature > Yesterday.temperature