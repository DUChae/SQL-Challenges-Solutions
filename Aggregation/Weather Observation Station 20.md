홀수일 경우 
	(n+1)/2
짝수일 경우
	n/2*(n/2+1)

SELECT 
FROM 
            (SELECT  ROW_NUMBER() OVER (ORDER BY LAT_N) AS numbering
                            ,COUNT( * ) OVER() AS n
                            , LAT_N
            FROM Station) sub

