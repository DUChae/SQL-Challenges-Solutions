SELECT id, movie, description, rating
<br/>
FROM Cinema
<br/>
WHERE MOD(id,2)=1
<br/>
AND description <> 'boring'
<br/>
ORDER BY rating DESC