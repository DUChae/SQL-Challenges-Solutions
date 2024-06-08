SELECT city <br/>
FROM Station <br/>
WHERE city REGEXP '^[aeiou]' AND city REGEXP '[aeiou]$'