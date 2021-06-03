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