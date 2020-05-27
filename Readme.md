# How to start

Create database :
```
Create database authorization character set utf8 collate utf8_unicode_ci;
```

Change db config in application.properties

```
...
spring.jpa.hibernate.ddl-auto=create-drop
spring.datasource.url=jdbc:mysql://localhost:3306/authorization
spring.datasource.username=root
spring.datasource.password=coderslab
spring.jpa.properties.hibernate.dialect = org.hibernate.dialect.MySQL5InnoDBDialect
...
```

# Init roles

Open endpoint - ONLY ONCE:
[http://localhost:8080/initData](http://localhost:8080/initData)

This will create two roles:
- ADMIN
- USER

and two users:
 - login: admin, password: admin 
 - login: user, password: user 

To test use endpoints:
- `/about` - you must be authorized
- `/admin` - you must have ADMIN role


## Hint
Names of roles need to have `ROLE` prefix when adding to DB ex.  want to use `ADMIN` - you need to save `ROLE_ADMIN` 
