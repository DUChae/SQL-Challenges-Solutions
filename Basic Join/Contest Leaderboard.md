total score of hacker = maximum score for all of the challenges

query : hacker_id, name, total score of the hacker
sort : total_score DESC, hacker_id ASC

exclude : total score of 0

SELECT H.hacker_id<br/>
            ,H.name<br/>
            ,SUM(sub.score) AS total_score<br/>
FROM <br/>
            (SELECT hacker_id, challenge_id, MAX(score) AS score<br/>
            FROM Submissions<br/>
            GROUP BY hacker_id, Challenge_id) sub<br/>
            INNER JOIN Hackers AS H ON H.hacker_id=sub.hacker_id<br/>
GROUP BY sub.hacker_id,h.name<br/>
HAVING total_score >0<br/>
ORDER BY total_score DESC, sub.hacker_id <br/>



