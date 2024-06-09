(SELECT city, LENGTH(city)<br/>
FROM Station<br/>
ORDER BY LENGTH(city) , city<br/>
LIMIT 1)<br/>
<br/>
UNION
<br/>
(SELECT city, LENGTH(city)<br/>
FROM Station <br/>
ORDER BY LENGTH(city) DESC , city<br/>
LIMIT 1)