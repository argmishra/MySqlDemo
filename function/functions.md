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