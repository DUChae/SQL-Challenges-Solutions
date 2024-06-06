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


With counter AS( <br/>
    SELECT Hackers.hacker_id <br/>
                , Hackers.name <br/>
                ,COUNT( * ) AS Challenges_created <br/>
    FROM Challenges  <br/>
    INNER JOIN Hackers ON Challenges.hacker_id = Hackers.hacker_id <br/>
    GROUP BY Hackers.hacker_id, hackers.name <br/>
)<br/>

SELECT counter.hacker_id <br/>
            , counter.name <br/>
            , counter.Challenges_created <br/>
FROM counter <br/>
WHERE Challenges_created=(SELECT MAX(Challenges_created) FROM counter) <br/>
OR Challenges_created IN (SELECT Challenges_created FROM counter GROUP BY Challenges_created HAVING COUNT( * ) =1) <br/>
ORDER BY counter.Challenges_created DESC, counter.hacker_id <br/>

 
