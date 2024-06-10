SELECT ROUND(S.LAT_N , 4)<br/>
FROM Station S<br/>
WHERE <br/>
		(SELECT COUNT(LAT_N)<br/>
		FROM Station<br/>
		WHERE LAT_N<S.LAT_N<br/>
		)<br/>
		=<br/>
		(SELECT COUNT(LAT_N) FROM STATION WHERE LAT_N>S.LAT_N)<br/>
<br/>

---
With using PERCENT_RANK()
<br/>
SELECT ROUND(LAT_N,4)<br/>
FROM <br/>
		(SELECT LAT_N,PERCENT_RANK() OVER (ORDER BY LAT_N ASC) AS R<br/>
		FROM Station<br/>
		)sub<br/>
WHERE R=0.5