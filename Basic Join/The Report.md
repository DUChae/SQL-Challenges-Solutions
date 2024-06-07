SELECT <br/>
            (CASE WHEN GRADE<8 THEN NULL <br/>
            ELSE S.NAME <br/>
             END) <br/>
             ,G.Grade <br/>
             ,S.marks <br/>
FROM Students AS S <br/>
INNER JOIN Grades AS G ON S.marks BETWEEN G.Min_mark AND G.Max_mark <br/>
ORDER BY G.Grade DESC,S.name,S.Marks <br/>