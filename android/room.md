# Theory
## Entity:

The Entity represents a table within the database, and has to be annotated with _@Entity._ Each Entity consist of a minimum of one field has to define a primary key.

## DAO (Database Access Object):

In Room you use data access objects to access and manage your data. The DAO is the main component of Room and includes methodes that offer access to your app's database. It has to be annotated with _@Dao_. DAOs are used instead of query builders and let you seperate different components of your database e.g. current data and statistics, which allows you to easily test your database.

`UserDao` provides the methods that the rest of the app uses to interact with data in the \`user\` table.

## Database:

Serves as the database holder an is the main accesspoint to your relational data. It has to be annotated with _@Database_ and extents the _RoomDatabase._ It also contains and returns the Dao (Database Access Object).
