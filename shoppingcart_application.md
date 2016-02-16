###Shopping Cart Application

Alton and Dave have teamed up to create an online store.

Your job is to find ten products for them to sell. Then create a database for those products. Next, create a dynamic web application using JPA to serve as a shopping cart for their online store.

Your application should allow the user to view a list of products (pictures are optional) and select a product to add to the shopping cart.

Each product should contain a name, description and price and any other information you want to add. The products must be stored in the database. After the application is complete you will be adding a new product and removing a product from the database. This change should not break your application.

The user should be able to browse the list, see product details and add the product to their cart. Then the user can go back to the list and shop more or can go to the cart to checkout.

You should have the following pages:
* Product List Page
* Product Details Page
* Shopping Cart Page that shows all the items in the shopping cart
* Order Confirmation  that shows the total amount of the items ordered

The order confirmation page should display a summary of the order.

Consider what code you can reuse from your previous project.

Be sure to include the sql scripts in your project. It is expected that another user could retrieve your file from GitHub to Eclipse and then run the sql script and your application should work.
How to create and access a cookie

Servlet code
```java
Cookie c = new Cookie("emailCookie", email);
c.setMaxAge(60*60); //set its age to 1 hour
c.setPath("/"); //allow the entire application to access it
response.addCookie(c);
```
JSP code

```java
<p>The email cookie: ${cookie.emailCookie.value}</p>
```

