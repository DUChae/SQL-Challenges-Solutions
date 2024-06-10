SELECT ROUND(LONG_W,4) <br/>
FROM Station<br/>
WHERE LAT_N=(SELECT MIN(LAT_N)<br/>
                            FROM Station<br/>
                            WHERE LAT_N>38.7780)
