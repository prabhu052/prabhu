# prabhu
java codes


package org.fincrony.connectionmgr;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.Statement;

class MySqlConnector{  
	
	
public MySqlConnector(){  
try{ 
	
   Class.forName("com.mysql.jdbc.Driver");  
   Connection con=DriverManager.getConnection("jdbc:mysql://localhost:3306/employee_details","root","prabhu");  
   
   System.out.println("Db connected");
   //here employee_details is database name, root is username and password is prabhu.
   Statement stmt=con.createStatement();  
   
    con.close();  
 } 
catch(Exception e){
	System.out.println(e);
	}  
}  
}  
