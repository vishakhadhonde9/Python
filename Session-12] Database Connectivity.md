# Database Connectivity- 
- Database connectivity in Python is a process of establishing a connection between Python applications and databases, enabling you to interact with the data.
- Common databases include SQLite, MySQL, PostgreSQL, and MongoDB.


# Install the Required Library:
- Depending on your database, you'll need a specific Python library:
    - MySQL: Install mysql-connector-python or pymysql.
    - PostgreSQL: Install psycopg2.
    - MongoDB: Install pymongo






import mysql.connector

# Connect to MySQL database
connection = mysql.connector.connect(
    host="localhost",
    user="your_username",
    password="your_password",
    database="your_database"
)

cursor = connection.cursor()

# Create a table
cursor.execute("CREATE TABLE IF NOT EXISTS users (id INT AUTO_INCREMENT PRIMARY KEY, name VARCHAR(255), age INT)")

# Insert data
cursor.execute("INSERT INTO users (name, age) VALUES (%s, %s)", ("Bob", 25))

# Fetch data
cursor.execute("SELECT * FROM users")
print(cursor.fetchall())

# Commit changes and close
connection.commit()
connection.close()



- The mysql.connector.connect() function establishes a connection to your MySQL database.
- The cursor is an object that allows you to interact with the MySQL database through Python. It is created from the connection object.
- Once the cursor is created, you can use it to send SQL commands to the database.
- VALUES (%s, %s): Placeholder syntax for inserting values securely.
%s is a placeholder for the actual data.
- fetchall() retrieves all the rows from the result of the query. It returns a list of tuples, where each tuple represents a row in the table.
