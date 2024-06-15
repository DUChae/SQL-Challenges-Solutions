total score of hacker = maximum score for all of the challenges

query : hacker_id, name, total score of the hacker
sort : score DESC, hacker_id ASC

exclude : total score of 0

SELECT H.hacker_id
            ,H.name
FROM submissions S
INNER JOIN hackers H ON S.hacker_id= H.hacker_id
ORDER BY S.score DESC , H.hacker_id

