1 column = Doctor<br/>
2 column = Professor<br/>
3 column= Singer<br/>
4 column = Actor<br/>

SELECT <br/>
            MAX(CASE WHEN Occupation='Doctor' THEN Name END) AS Doctor<br/>
            ,MAX(CASE WHEN Occupation='Professor' THEN Name END) AS Professor<br/>
            ,MAX(CASE WHEN Occupation='Singer' THEN Name END) AS Singer<br/>
            ,MAX(CASE WHEN Occupation='Actor' THEN Name END) AS Actor<br/>
FROM <br/>
            (SELECT Occupation<br/>
                        ,name<br/>
                        ,ROW_NUMBER() OVER (PARTITION BY Occupation ORDER BY Name) AS Numbering<br/>
            FROM Occupations<br/>
            )sub<br/>
GROUP BY Numbering