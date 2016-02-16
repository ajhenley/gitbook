# JSP Servlet Interaction Review

Bank Balance Lookup exercise

Use MVC architecture (Model View Controller)

The model is the database…. I’m giving that to you as a class. Do not connect to Oracle.

Bean: Bank Customer

Business Logic: Bank Customer Lookup

Servlet that populates the bean and forwards to the appropriate JSP page

    Reads CustomerID, calls BankCustomerLookup’s data-access code to obtain BankCustomer
    Uses current balance to decide on appropriate result page

JSP pages to display the results:

    Negative Balance: Warning Page
    Regular Balance: standard Page
    High Balance: page with advertisements added
    Unknown customerID: error page

Here is some code to get you started:

package BankBalanceLookup;

public interface CustomerLookupService {
 
public Customer findCustomer(String id);

}

 

package BankBalanceLookup;

import java.util.HashMap;
import java.util.Map;

public class CustomerSimpleMap implements CustomerLookupService {
 
private Map<String, Customer> customers;

public CustomerSimpleMap() {
 customers = new HashMap<String, Customer>();
 
addCustomer(new Customer("id001", "Harry", "Hacker", -3456.78));
 
addCustomer(new Customer("id002", "Codie", "Coder", 1234.56));
 
addCustomer(new Customer("id003", "Polly", "Programmer", 987654.32));
 
}
 
 
@Override
 
public Customer findCustomer(String id) {
 if (id!=null){
 return(customers.get(id.toLowerCase()));
 }else{
 return null;
 }}
 
 private void addCustomer(Customer customer) {
 customers.put(customer.getId(), customer);
 }}