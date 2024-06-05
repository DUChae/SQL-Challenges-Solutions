SELECT DISTINCT city <br/>
FROM station <br/>
WHERE city NOT LIKE 'a%' <br/>
AND city NOT LIKE 'e%' <br/>
AND city NOT LIKE 'i%' <br/>
AND city NOT LIKE 'o%' <br/>
AND city NOT LIKE 'u%' <br/>
AND city NOT LIKE '%a' <br/>
AND city NOT LIKE '%e' <br/>
AND city NOT LIKE '%i' <br/>
AND city NOT LIKE '%o' <br/>
AND city NOT LIKE '%u' 