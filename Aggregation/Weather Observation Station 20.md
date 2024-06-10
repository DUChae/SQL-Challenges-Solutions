홀수일 경우 
	(n+1)/2
짝수일 경우
	n/2*(n/2+1)

SELECT 
		(Case WHEN MOD(COUNT(LAT_N)),2=0
					THEN
		)
FROM Station
ORDER BY LAT_N