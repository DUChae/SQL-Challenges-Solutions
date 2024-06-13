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


