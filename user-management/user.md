## Show User
```mysql
select user from mysql.user;
```

## Create User
```mysql
create user anurag@localhost identified by 'password';
```

## Grant PRIVILEGES to User
```mysql
GRANT ALL PRIVILEGES ON * . * TO anurag@localhost; 
```

## Show PRIVILEGES of User
```mysql
SHOW GRANTS for anurag@localhost;
```

## Revert PRIVILEGES to User
```mysql
revoke all, grant option from anurag@localhost; 
```

## Drop User
```mysql
drop user anurag@localhost;
```

## Change Password
```mysql
SET PASSWORD FOR 'anurag'@'localhost' = 'test';
FLUSH PRIVILEGES;  
```