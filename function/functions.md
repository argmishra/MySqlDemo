## IF Function
```mysql
SELECT first_name,
IF(age>25,'Yes','No') FROM user; 
```

## IFNULL Function
```mysql
SELECT ifnull (first_name, last_name) FROM user; 
```

## NULLIF Function
```mysql
SELECT first_name, NULLIF (age,33) result FROM user;  
```

## CASE Function
```mysql
SELECT first_name,  
 CASE age   
    WHEN 16 THEN 'No'   
    WHEN 33 THEN 'Yes'   
    ELSE 'Ok'   
END AS eligble from user;
```

## Count Aggregate Function
```mysql
select count(*) from employee;
```
OR
```mysql
select count(name) from employee;
```
OR
```mysql
select count(distinct name) from employee;
```

## Sum Aggregate Function
```mysql
select sum(age) from employee
```

## Average Aggregate Function
```mysql
select avg(age) from employee;
```

## Min  Aggregate Function
```mysql
select min(age) from employee;
```

## Max Aggregate Function
```mysql
select max(age) from employee;
```

## Group Concat Aggregate Function
```mysql
SELECT id, name, occupation, age, GROUP_CONCAT(age + id) as "key" FROM employee group by id;
```

## Top Aggregate Function
```mysql
select * from employee limit 1;
```

## Last Aggregate Function
```mysql
select * from employee order by id desc limit 1;
```