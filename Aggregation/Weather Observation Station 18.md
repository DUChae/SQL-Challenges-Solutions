P1(a,b) / P2(c,d)<br/>
a= MIN(LAT_N)<br/>
b=MIN(LONG_W)<br/>
c=MAX(LAT_N)<br/>
d=MAX(LONG_W)<br/>
<br/>
Manhattan Distance : p1 at (x1, y1) and p2 at (x2, y2), it is |x1 - x2| + |y1 - y2|.<br/>
결과값 =ROUND(?,4)<br/>



SELECT ROUND(ABS(a-c)+ABS(b-d),4)<br/>
FROM(SELECT MIN(LAT_N) AS a<br/>
                ,MIN(LONG_W) AS b<br/>
                ,MAX(LAT_N) AS c<br/>
                ,MAX(LONG_W) AS d<br/>
            FROM Station) sub
