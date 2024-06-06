SELECT id, <br/>
<br/>
SUM(CASE WHEN month='Jan' THEN revenue ELSE NULL END) AS Jan_Revenue, <br/>
<br/>
SUM(CASE WHEN month='Feb' THEN revenue ELSE NULL END) AS Feb_Revenue, <br/>
<br/>
SUM(CASE WHEN month='Mar' THEN revenue ELSE NULL END) AS Mar_Revenue, <br/>
<br/>
SUM(CASE WHEN month='Apr' THEN revenue ELSE NULL END) AS Apr_Revenue, <br/>
<br/>
SUM(CASE WHEN month='May' THEN revenue ELSE NULL END) AS May_Revenue, <br/>
<br/>
SUM(CASE WHEN month='Jun' THEN revenue ELSE NULL END) AS Jun_Revenue, <br/>
<br/>
SUM(CASE WHEN month='Jul' THEN revenue ELSE NULL END) AS Jul_Revenue, <br/>
<br/>
SUM(CASE WHEN month='Aug' THEN revenue ELSE NULL END) AS Aug_Revenue, <br/>
<br/>
SUM(CASE WHEN month='Sep' THEN revenue ELSE NULL END) AS Sep_Revenue, <br/>
<br/>
SUM(CASE WHEN month='Oct' THEN revenue ELSE NULL END) AS Oct_Revenue, <br/>
<br/>
SUM(CASE WHEN month='Nov' THEN revenue ELSE NULL END) AS Nov_Revenue, <br/>
<br/>
SUM(CASE WHEN month='Dec' THEN revenue ELSE NULL END) AS Dec_Revenue <br/>
<br/>
FROM department <br/>
<br/>
GROUP BY id