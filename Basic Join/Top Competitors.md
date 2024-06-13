출력문 : hacker_id, name of hackers(하나 이상의 챌린지를 만점받은)
정렬 : total number of challenges in which the hacker earned a full score DESC, hacker_id ASC

테이블 
Hackers, Difficulty , Challenges, Submissions

Hackers

| Column    | Type    |
| --------- | ------- |
| hacker_id | Integer |
| name      | String  |

Difficulty

| Column           | Type        |
| ---------------- | --------- |
| difficulty_level | Int   er    |
| score        Integer   egerg   |

Challenges

| Column           | Type    |
| ---------------- | ------- |
| challenge_id     | Integer |
| hacker_id        | Integer |
| difficulty_level | Integer |

SELECT S.hacker_id <br/>
            , H.name<br/>
FROM Submissions AS S<br/>
        INNER JOIN Challenges AS C ON C.challenge_id=S.challenge_id<br/>
        INNER JOIN Difficulty AS D ON C.difficulty_level = D.difficulty_level<br/>
        INNER JOIN Hackers AS H ON H.hacker_id=S.hacker_id<br/>
WHERE S.score=D.score<br/>
GROUP BY S.hacker_id, H.name<br/>
HAVING COUNT(S.challenge_id)>1<br/>
ORDER BY COUNT(S.hacker_id) DESC, S.hacker_id
