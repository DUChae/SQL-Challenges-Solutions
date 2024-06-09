SELECT DISTINCT city <br/>
FROM Station <br/>
WHERE city NOT REGEXP '^[aeiou]' OR city NOT REGEXP '[aeiou]$'