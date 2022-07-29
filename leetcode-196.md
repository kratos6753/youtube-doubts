Link to the problem: https://leetcode.com/problems/delete-duplicate-emails

Link to my video solution: https://www.youtube.com/watch?v=UMpgB5JnttM

**Input:** Person table

| id | email            |
|----|------------------|
| 1  | john@example.com |
| 2  | bob@example.com  |
| 3  | john@example.com |

**Person P1 X Person P2**
| p1.id | p1.email         | p2.id | p2.email         |
|-------|------------------|-------|------------------|
| 1     | john@example.com | 1     | john@example.com |
| 1     | john@example.com | 2     | bob@example.com  |
| 1     | john@example.com | 3     | john@example.com |
| 2     | bob@example.com  | 1     | john@example.com |
| 2     | bob@example.com  | 2     | bob@example.com  |
| 2     | bob@example.com  | 3     | john@example.com |
| 3     | john@example.com | 1     | john@example.com |
| 3     | john@example.com | 2     | bob@example.com  |
| 3     | john@example.com | 3     | john@example.com |

**Person P1 X Person P2 where P1.email = P2.email**
| p1.id | p1.email         | p2.id | p2.email         |
|-------|------------------|-------|------------------|
| 1     | john@example.com | 1     | john@example.com |
| 1     | john@example.com | 3     | john@example.com |
| 2     | bob@example.com  | 2     | bob@example.com  |
| 3     | john@example.com | 1     | john@example.com |
| 3     | john@example.com | 3     | john@example.com |

**Person P1 X Person P2 where P1.email = P2.email and P1.id < P2.id**
| p1.id | p1.email         | p2.id | p2.email         |
|-------|------------------|-------|------------------|
| 1     | john@example.com | 3     | john@example.com |

**Now delete P2 from the table**
That is, delete the record with id = 3 shown in the above table.

Ans:- **delete p2 from Person p1, Person p2 where p1.email = p2.email and p1.id < p2.id;**
