# postgres-basic-command
Basic Commands for using postgreSQL

### Initially 'postgres' is the superuser 
#### Login as 'postgres' with the password set when installing postgresql
```
psql -U postgres
```

#### Create a new user
```
create user tanveer with password '123456';
```

#### List all users
```
\du
```

#### Giving superuser power to the new user
```
alter user tanveer with superuser;
```

#### Creating new database
```
create database test_db;
```

#### Since we create test_db with postgres we need to give priviledges of test_db to tanveer
```
GRANT ALL PRIVILEGES ON DATABASE test_db to tanveer;
```

#### List all databases
```
\l
```

#### Login as specifiq user with specifiq database
```
psql -U tanveer -d test_db
```

#### List all tables in a database after login with that database
```
\d
```

