##  AND Conditions
```mysql
select * from employee where id=1 AND age=29;
```

##  OR Conditions
```mysql
select * from employee where id=1 OR age=55;
```

##  AND/OR Conditions
```mysql
select * from employee where id=1 OR age=31 and name='Vinit';
```

##  LIKE Conditions
```mysql
select * from employee where name like 'A%';
```

##  NOT Conditions
```mysql
select * from employee where name not like 'A%';
```

##  IN Conditions
```mysql
select * from employee where id IN (1,4);
```

##  NOT EQUALS Conditions
```mysql
select * from employee where id!=1 OR age<>29;
```

##  IS Conditions
```mysql
select * from employee where occupation is null;
```

##  IS NOT Conditions
```mysql
select * from employee where occupation is not null;
```

##  BETWEEN Conditions
```mysql
select * from employee where age between 20 AND 50;
```