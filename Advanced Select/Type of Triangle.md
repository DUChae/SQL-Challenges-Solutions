SELECT <br/>
            CASE <br/>
                    WHEN A+B<=C OR A+C<=B OR B+C<=A THEN 'Not A Triangle' <br/>
                    WHEN A=B AND B=C THEN 'Equilateral' <br/>
                    WHEN A=B OR A=C OR B=C THEN 'Isosceles' <br/>
                    ELSE 'Scalene' <br/>
            END <br/>
            <br/>
FROM triangles 
