a=MIN(LAT_N)<br/>
b=MAX(LAT_N)<br/>
c=MIN(LONG_W)<br/>
d=MAX(LONG_W)<br/>

FORMAT(SQRT(POW((a-b),2) + POW((c-d),2)),4)<br/>
<br/>

SELECT FORMAT(SQRT(POW((a-b),2) + POW((c-d),2)),4)<br/>
FROM<br/>
                (SELECT MIN(LAT_N) AS a<br/>
                            ,MAX(LAT_N) AS b<br/>
                            ,MIN(LONG_W) AS c<br/>
                            ,MAX(LONG_W) AS d<br/>
                FROM Station)sub