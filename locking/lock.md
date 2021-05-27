Lock Table
```mysql
lock table employee READ;
```
OR
```mysql
lock table employee WRITE;
```

Unlock Table
```mysql
unlock tables;
```

Lock User
```mysql
alter user anurag@localhost account lock;  
```

UnLock User
```mysql
alter user anurag@localhost account unlock;  
```