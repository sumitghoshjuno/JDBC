# How to create connection Using Java app
# JDBC
import java.sql.*;
class FirstJDBC{

    /**
     * @param args
     */
    public static void main(String args[])
{
try
{
    //load the driver:
    Class.forName("com.mysql.jdbc.Driver");
    //creating a connection
    String url="jdbc:mysql://localhost:3306/sanu";
    String username="root";
    String password="root";

    Connection con =DriverManager.getConnection(url,username,password);
    if (con.isClosed())
    {
        System.out.println("Connection is Closed");
    }
    else
    {
       System.out.println("Connection is created"); 
    }
}
catch(Exception e)
    {
        e.printStackTrace();
    }
}
}

