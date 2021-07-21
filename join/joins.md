## INNER JOIN
```mysql
SELECT o.location, o.staff, n.type, n.working    
FROM office o   
INNER JOIN number n    
ON o.office_id = n.number_id; 
```

## LEFY JOIN
```mysql
SELECT o.location, o.staff, n.type, n.working    
FROM office o   
LEFT JOIN number n    
ON o.office_id = n.number_id; 
```

## RIGHT JOIN
```mysql
SELECT o.location, o.staff, n.type, n.working    
FROM office o   
RIGHT JOIN number n    
ON o.office_id = n.number_id; 
```

## CROSS JOIN
```mysql
SELECT o.location, o.staff, n.type, n.working 
FROM office o  
CROSS JOIN number n;
```

## SELF JOIN
```mysql
SELECT o1.office_id, o1.location
FROM office AS o1, office o2  
WHERE o1.office_id=o2.office_id;
```

## EQUI JOIN
```mysql
SELECT o.location, o.staff, n.type, n.working
FROM office as o   
INNER JOIN number as n    
ON o.office_id = n.number_id;
```

## NATUTAL JOIN
```mysql
SELECT * FROM office NATURAL JOIN number; 
```

## UPDATE JOIN
```mysql
UPDATE office o
INNER JOIN number n 
ON o.office_id = n.number_id  
SET staff = 35;
```

## DELETE JOIN
```mysql
DELETE office, number FROM office
INNER JOIN number ON office.office_id=number.number_id
WHERE office.office_id = 3; 
```

## Test Data
```mysql
CREATE TABLE office (office_id INT , location varchar(50), staff INT);  
CREATE TABLE number (number_id INT, working boolean, type varchar(50)); 

INSERT INTO office(office_id, location, staff) VALUES  
(1, 'India', 22),  
(2, 'Ireland', 2), 
(3, 'UK', 12),
(4, 'US', 2); 

INSERT INTO number (number_id, type, working) VALUES  
(1, 'mobile', true),  
(1, 'phone', false),  
(2, 'mobile', true),  
(2, 'phone', false),  
(2, 'fax', true),
(3, 'mobile', true),
(5, 'satalite', true);
```