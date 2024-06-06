SELECT H.hacker_id, H.name , COUNT( * )  AS Challenges_created <br/>
FROM Hackers AS H <br/>
        INNER JOIN Challenges AS C <br/>
        ON H.hacker_id=C.hacker_id <br/>
GROUP BY H.hacker_id, H.name  <br/>
HAVING Challenges_created=(SELECT MAX(Challenges_created) <br/>
FROM <br/>
(SELECT  hacker_id, COUNT( * ) AS Challenges_created <br/>
 FROM Challenges <br/>
 GROUP BY Hacker_id) sub) <br/>
OR <br/>
Challenges_created IN (SELECT Challenges_created <br/>
FROM <br/>
            (SELECT  hacker_id, COUNT( * ) AS Challenges_created <br/>
             FROM Challenges <br/>
             GROUP BY Hacker_id) sub <br/>
GROUP BY Challenges_created <br/>
 HAVING COUNT( * ) = 1 
)<br/>
ORDER BY Challenges_created DESC, hacker_id


---


 
