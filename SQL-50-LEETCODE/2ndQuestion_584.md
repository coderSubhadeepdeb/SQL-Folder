# Find Customer Referee (Leetcode 584)

**Table: Customer**

| Column Name | Type    |
|-------------|---------|
| id          | int     |
| name        | varchar |
| referee_id  | int     |

- In SQL, `id` is the `primary key` column for this table.
- Each row of this table indicates the `id` of a customer, their `name`, and the id of the customer who `referred` them.

**Question**:<br> 
Find the names of the customer that are either:
- referred by any customer with id != 2.
- not referred by any customer.
Return the result table in any order.

**Input:**
Customer table:
| id | name | referee_id |
|----|------|------------|
| 1  | Will | null       |
| 2  | Jane | null       |
| 3  | Alex | 2          |
| 4  | Bill | null       |
| 5  | Zack | 1          |
| 6  | Mark | 2          |

**OUtput**:
| name |
|------|
| Will |
| Jane |
| Bill |
| Zack |

## Approach: 
- Just simply select the `name` from the table such that for each row  `referee_id is NULL` or `reeferee_id != 2`

##Code Snippet (MySQL):

```sql
SELECT name FROM Customer  
WHERE referee_id IS NULL OR referee_id != 2; -- referee_id = NULL is not valid syntax. Always use IS NULL or IS NOT NULL