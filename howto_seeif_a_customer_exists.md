# How to see if a customer exists


How to see if a customer exists

//see if customer exists
TypedQuery<Long> query = em.createQuery("SELECT COUNT(c) FROM DemoCustomer c WHERE c.customerId = 2L", Long.class);
long total = query.getSingleResult();
if (total>0)
{
out.printf("%s", "Customer exists");
}else{
out.printf("%s", "Customer does not exist");
}
