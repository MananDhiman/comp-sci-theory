# Spring Intro

## Inversion of Control

UserDAO didn’t have to worry about finding dependencies at all? Instead of actively calling Application.INSTANCE.dataSource(), your UserDAO could shout (somehow) that it needs one, but has no control anymore when/how/where it gets it from?

before
```java
class UserDao {
	
public User findById(Integer id) {
        try (Connection connection = newDataSource().getConnection()) { // (1)
               PreparedStatement selectStatement = connection.prepareStatement("select * from users where id =  ?");
               // TODO execute the select , handle exceptions, return the user
        }
    }

public DataSource newDataSource() {
        MysqlDataSource dataSource = new MysqlDataSource(); // (3)
        dataSource.setUser("root");
        dataSource.setPassword("s3cr3t");
        dataSource.setURL("jdbc:mysql://localhost:3306/myDatabase");
        return dataSource;
    }
}
```

after
```java
public class UserDao {

    private DataSource dataSource;

    public UserDao(DataSource dataSource) { // (1)
        this.dataSource = dataSource;
    }

public User findById(Integer id) {
    try (Connection connection = dataSource.getConnection()) { // (2)
        PreparedStatement selectStatement = connection.prepareStatement("select * from users where id =  ?");
               // TODO execute the select etc.
        }
    }
}
```

## Dependency Injection
if someone knew that your UserDAO has a DataSource constructor dependency and knew how to construct one? And then magically construct both objects for you: A working DataSource and a working UserDao? That someone is a dependency injection container