## Where clause
```mysql
select * from employee where (name='Anurag' and age=29 ) or occupation='Lead';
```

## Distinct clause
```mysql
select distinct occupation from employee;
```

## From clause
```mysql
select * from employee;
```

## Order by clause
```mysql
select * from employee order by name asc, id desc;
```

## Group By clause
```mysql
SELECT name, AVG(age) FROM employee GROUP BY name;
```

## Having clause
```mysql
SELECT name, AVG(age) FROM employee GROUP BY name having AVG(age) > 32;
```
