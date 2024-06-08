SELECT DISTINCT city <br/>
FROM station <br/>
WHERE city LIKE 'a%' <br/>
OR city LIKE'e%' <br/>
OR city LIKE'i%' <br/>
OR city LIKE'o%' <br/>
OR city LIKE'u%' <br/>


---
 WIth using REGEXP <br/>
 SELECT DISTINCT city <br/>
FROM station <br/>
WHERE city REGEXP '^[aeiou].*'