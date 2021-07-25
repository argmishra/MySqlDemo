## Insert Table - Single Row
```mysql
insert into employee (id, name, occupation, age) values (1, 'Anurag', 'Developer', 39);
```

## Insert Table - Multiple Row
```mysql
insert into employee (id, name, occupation, age) values 
(1, 'Anurag', 'Developer',29),
(2, 'Abhinav', 'Manager', 33),
(3, 'Vinit', 'Engineer', 31),
(4, 'Jugal', 'Lead', 55),
(1, 'Anurag', 'Developer',29),
```

## Update Table
```mysql
update employee set name="Anu", age=29 where id=1;
```

## Delete Table
```mysql
delete from employee where id=1;
```

## Show Table
```mysql
select * from employee where id=2;
```

## Replace Table
```mysql
replace into employee (id, age) values (3, 400);
```

## Insert Table by Select
```mysql
insert into user (name) select name from employee where id=2;
```

## Upsert Table
```mysql
insert ignore into employee (id, name, occupation, age) values 
(1, 'Anurag', 'Developer',29);
```

## Cast
```mysql
SELECT CAST("2018-11-30" AS DATE);  
```

## Convert
```mysql
SELECT CONVERT("2018-11-30", DATETIME);  
```

## Extract
```mysql
SELECT EXTRACT(MONTH FROM '2020-07-15 08:06:44') AS MONTH;
```

## COALESCE
```mysql
SELECT COALESCE(NULL, 1, 2, 'MySQL', NULL, 'JAVA', NULL);   
```

## Alias
```mysql
select id as "user_id", first_name as "name" from user;
```

## Explain
```mysql
EXPLAIN select * from user;
```

## Random
```mysql
SELECT * FROM user ORDER BY RAND()
```
