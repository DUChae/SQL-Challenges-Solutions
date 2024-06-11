```
There are a total of [occupation_count] [occupation]s.
```
1. 이름을 알파벳순으로 정렬 후 이름 옆 이니셜통해 직업표기
2. 직업별로 몇명있는지 
3. 같은 수라면 알파벳순으로
<br/>
SELECT CONCAT(Name, '(', LEFT(Occupation, 1), ')')<br/>
FROM OCCUPATIONS<br/>
ORDER BY Name ;<br/>
<br/>

SELECT CONCAT('There are a total of ', COUNT(Occupation), ' ', LOWER(Occupation), 's.')<br/>
FROM OCCUPATIONS<br/>
GROUP BY Occupation<br/>
ORDER BY COUNT(Occupation), Occupation;


