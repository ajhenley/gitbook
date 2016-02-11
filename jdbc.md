<!--djw: 
1. todo: need to include correct connection string
2. todo: need to include link for ojdbc6.jar http://www.oracle.com/technetwork/middleware/oedq/downloads/edq-vm-download-2424092.html
-->
###Get JDBC running on the virtual machine
To develop Java applications which access the Oracle database you will need to download the ojdbc6.jar library from Oracle. You'll need to include that library in your eclipse project.

Here is some example code that will work with the virtual machine. Create a new eclipse project called OracleJDBCTestProject. Then create a class called TestOracleJDBC. Copy the following code to that class. 

This code will connect to the database and return a result. Or an error. You must fix the error before you can continue to work with Oracle and Java. The most common source of errors is the connection string. 

####What is a connection string?
In the code below the connection string is ```jdbc:oracle:thin:testuser/blue123@localhost```. The connection string contains parameters. ODBC.jar library will use those parameters to connect with your instance of the  Oracle database. 

{%ace edit=true, lang='sql'%}
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.ResultSet;
import java.sql.SQLException;
import java.sql.Statement;

public class TestOracleJDBC {
	public static void main(String[] args) {
		Connection con = null;
		Statement stmt = null;
		ResultSet rs = null;
		try{
			Class.forName("oracle.jdbc.driver.OracleDriver");
			con = DriverManager.getConnection("jdbc:oracle:thin:testuser/blue123@localhost");
			stmt = con.createStatement();
			rs = stmt.executeQuery("select * from person");
			while(rs.next()){
				System.out.println(rs.getInt(1) + "\t");
				System.out.println(rs.getString(2));
			}
			}catch (SQLException e) {
				e.printStackTrace();
			}catch (ClassNotFoundException e) {
				e.printStackTrace();
		} finally {
			try {
				rs.close();
				stmt.close();
				con.close();
			}catch(SQLException e){
				e.printStackTrace();
			}
		}
	}
}
{%endace%}