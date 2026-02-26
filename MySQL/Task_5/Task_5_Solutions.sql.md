
# 1- Duplicate Emails

```
select email from Person group by email having  count(email)>1  ;

```
       
# 2-Delete Duplicate Emails
```

DELETE P1 FROM PERSON P1, PERSON P2
	
	WHERE P1.EMAIL=P2.EMAIL AND P1.ID>P2.ID;
```
# 3-Nth Highest Salary
                 
```
     CREATE FUNCTION getNthHighestSalary(N INT) RETURNS INT
	
	 BEGIN
	
	 set N=N-1;
	
	  RETURN (
	
	    select distinct  salary from Employee order by  salary desc limit 1 offset N);END
```
	
#  4-Rank Scores
```
select score ,
	
	      DENSE_RANK() OVER (
	
	           ORDER BY score  DESC
	
	    )   AS" rank"
	
	  FROM Scores;
```
# 5-Department Highest Salary
```
	
	SELECT d.name as  Department, e.name as Employee, e.salary AS Salary
	
	FROM (
	
	    SELECT name, departmentId, salary,
	
	           RANK() OVER (PARTITION BY departmentId ORDER BY salary DESC) AS rnk
	
	    FROM Employee) as e
	
	JOIN Department as d ON e.departmentId = d.id
	
	WHERE e.rnk = 1;

```