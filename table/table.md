Create Table
```mysql
create table if not exists employee (
id int NOT NULL auto_increment,
name varchar(45) NOT NULL,
occupation varchar(45) NOT NULL,
age int NOT NULL,
primary key(id)
);
```

Show Tables
```mysql
show tables;
```

Show Table Structure
```mysql
describe employee;
```
OR
```mysql
show columns from employee;
```

Add Column
```mysql
alter table employee add city varchar(40) NOT NULL;
```
OR
```mysql
alter table employee add address varchar(40) NOT NULL
after name,
add address long NOT NULL;
```

Modift Column
```mysql
alter table employee modify address varchar(80) NULL;
```

Drop Column
```mysql
alter table employee drop column salary;
```

Rename Column
```mysql
alter table employee change column city country varchar(80) NULL;
```

Rename Table
```mysql
alter table employee rename to user;
```
OR
```mysql
rename table user to employee;
```

Truncate Table
```mysql
INSERT INTO employee ( id, name, address, occupation, age, country)
VALUES (1, 'Anurag', 'Limerick', 'Developer', 29, 'India');
truncate table employee;
```

Drop Table
```mysql
drop table employee;
```

Copy Table
```mysql
CREATE TABLE IF NOT EXISTS duplicate_table   
SELECT * FROM original_table;  
```

Create View
```mysql
create view argmishra as select name from employee;
```
