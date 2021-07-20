## Unique Key - One Column
```mysql
CREATE TABLE car (id int NOT NULL unique, name varchar(45));  
INSERT INTO car(id, name) VALUES (1,'Getz');
INSERT INTO car(id, name) VALUES (1,'ALTO');
```

## Unique Key - Multiple Columns
```mysql
CREATE TABLE truck (id int, price int, name varchar(45), CONSTRAINT uc_id_price Unique(id, price) );  
INSERT INTO truck(id, price, name) VALUES (1,12, 'MH');
INSERT INTO truck(id, price, name) VALUES (1,12, 'Benz');
```

## Unique Key - Delete
```mysql
ALTER TABLE car DROP INDEX id;  
```

## Primary Key - One Column
```mysql
CREATE TABLE login(id INT PRIMARY KEY, username VARCHAR(40), password VARCHAR(55));  
INSERT INTO login(id, username, password) VALUES (1, 'Anu', 123);
INSERT INTO login(id, username, password) VALUES (1, 'Raf', 4444);
```

## Primary Key - Multiple Columns
```mysql
CREATE TABLE register (id int, age int, name varchar(45), Primary Key(id, name) );  
INSERT INTO register(id, age, name) VALUES (1,12, 'Sonu');
INSERT INTO register(id, age, name) VALUES (1,22, 'Sonu');
```

## Primary Key - Delete
```mysql
ALTER TBLE login DROP PRIMARY KEY; 

```

## Foreign Key
```mysql
CREATE TABLE customer (id INT NOT NULL AUTO_INCREMENT, name varchar(50) NOT NULL, PRIMARY KEY (ID));  
CREATE TABLE contact (id INT, cus_id INT, type varchar(50) NOT NULL, INDEX par_ind (cus_id), CONSTRAINT fk_customer FOREIGN KEY (cus_id) REFERENCES customer(id) ON DELETE CASCADE ON UPDATE CASCADE); 

INSERT INTO customer(name) VALUES  
('Anu'),  
('Sonu');

INSERT INTO contact (cus_id, type) VALUES  
(1, 'new'),  
(2, 'old'),  
(2, 'no');
```

## Foreign Key - Delete
```mysql
ALTER TABLE contact DROP FOREIGN KEY fk_customer;  

```