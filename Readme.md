# How to start

Create database :
```
Create database authorization character set utf8 collate utf8_unicode_ci;
```

Change db config in application.properties

```
...
spring.jpa.hibernate.ddl-auto=create-drop
spring.datasource.url=jdbc:mysql://localhost:3306/db_example
spring.datasource.username=root
spring.datasource.password=coderslab
spring.jpa.properties.hibernate.dialect = org.hibernate.dialect.MySQL5InnoDBDialect
...
```

