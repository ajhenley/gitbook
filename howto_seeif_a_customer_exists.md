###How to see if a customer exists

If you want to know if Customer #2 exists in the database then here's how you can query the database using JPQL. In this code example the JPQL statement will always return a non-negative value. If the customer does not exist then the query will return 0. Otherwise it will return a count of the number of times the customer does exist. You will retieve the count in the total variable. Next you just compare the value of that variable to determine what action you should take.

```java
//see if customer exists
TypedQuery<Long> query = em.createQuery("SELECT COUNT(c) FROM DemoCustomer c WHERE c.customerId = 2L", Long.class);
long total = query.getSingleResult();
if (total>0)
{
    out.printf("%s", "Customer exists");
}else{
    out.printf("%s", "Customer does not exist");
}
```

