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

With test AS
            (SELECT  ROW_NUMBER() OVER (ORDER BY LAT_N) AS numbering
                            ,COUNT(*) OVER() AS n
                            , LAT_N
            FROM Station) 
            
SELECT 
            CASE WHEN n%2=1 THEN
                                (SELECT LAT_N
                                FROM test
                                 WHERE numbering=(n+1)/2
                                )
                        ELSE
                                (
                                SELECT AVG(LAT_N)
                                    FROM test
                                    WHERE numbering IN((n/2) * ((n/2)+1) )
                        END    )
FROM test
ORDER BY n