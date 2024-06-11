```
There are a total of [occupation_count] [occupation]s.
```
1. 이름을 알파벳순으로 정렬 후 이름 옆 이니셜통해 직업표기
2. 직업별로 몇명있는지 
3. 같은 수라면 알파벳순으로

이니셜
SELECT SUBSTRING(Occupation,1,1)
FROM OCCUPATIONS