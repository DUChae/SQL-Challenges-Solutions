SELECT N, <br/>
            (CASE WHEN P IS NULL THEN 'Root'<br/>
            WHEN N NOT IN (<br/>
                                            SELECT DISTINCT P<br/>
                                            FROM BST<br/>
                                            WHERE P IS NOT NULL  <br/>
                                        ) THEN 'Leaf'<br/>
             ELSE 'Inner'<br/>
            END)<br/>
FROM BST<br/>
ORDER BY N
