Q1: What is JDBC 
Ans: Java Data Base Connectivity is a specification given in the form of Abstraction API to achieve loose coupling b/w Java application and DB server.

JDBC API contains Interfaces and Helper Classes in the form of jar file.
Distributed in two different packages 1) Java.sql 2) javax.sql

Advantages: Achieve loose coupling and Platform Independent
--------------------------------------------------------------------------------------------------------------------

Q2: What are the Interfaces of JDBC API?
Ans: 1) Driver, 2) Connection, 3) Statement, 4) PreparedStatement, 5) CallableStatement, 6) ResultSet  etc...
--------------------------------------------------------------------------------------------------------------------

Q3: Which is the helper class in JDBC API and what are the heper methods presnt in it?
Ans: DriverManager is the Helper class and it has two static helper methods a)getConnection("url") b) registerDriver.
     There are 3 overloaded method of getConnection which takes params as a)(String url) b)(String url, Properties info) b)(String url,String user,String password)
--------------------------------------------------------------------------------------------------------------------

Q4: What are the Steps for JDBC
Ans: There are 6 steps in JDBC
    * Load and Register the Driver class.
        Eg: Class.forName("com.sql.jdbc.Driver")
    * Establish the connection with DB Server. 
        Eg: java.sql.Connection con =DriverManager.getConnection("jdbc:mysql://localhost:3306?user=root&password=----")
    * Create a statement or platform. 
        Eg: java.sql.Statement stmt= con.createStatement(); #here platform can be created either by using Statement/PreparedStatement/CallableStatement Interfaces
    * Execute the SQL queries/statements. 
        Eg: stmt.execute("Any Query here")/stmt.executeUpdate("Only DML Query here")/stmt.executeQuer("only DQL query")
    * Process the resultant data. 
        Note: (Select Query) and fetch the data and process
    * Close all the costly resources
        Note: i.e, Interfaces as it uses the Stream (System) to connect w/ DB Eg: con.close();/stmt.close()/ etc... in finaly block.
-------------------------------------------------------------------------------------------------------------------

Q: What are the difference b/w  statements
Q: What is the difference b/w execute(), executeUpdate() and executeQuery()
Q: Brief about all the Interfaces in JDBC API
Q: How to set value for Placeholder and what are the rules?
Q: Name few Driver classes provided by DB vendors
Q: What is next and absolute method
Q: Which method is used to fetch processed/resultant data from cursor/buffer memory
Q: Explain getXXX and setXXX method and it's retur type