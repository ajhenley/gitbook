<!-- djw: -->
###What is JPQL?
The Java Persistence Query Language (JPQL) is the query language defined by JPA. JPQL is similar to SQL  but operates on objects, attributes and relationships instead of tables and columns. JPQL can be used for reading (SELECT), as well as updates (UPDATE) and deletes (DELETE). This course will focus on creating dynamic queries using the EntityManager createQuery() API.

The Java Persistence query language defines queries for entities and their persistent state. The query language allows you to write portable queries that work for any database. An application developed with JPQL and Oracle does not have to be modified when the database is changed to Microsoft SQL Server.

####Creating Queries Using the Java Persistence Query Language
Select queries can be used to read objects from the database. Select queries can return a single object or data element, a list of objects or data elements, or an object array of multiple objects and data.

The ```EntityManager.createQuery()``` method is used within your class to query the database using Java Persistence query language queries.  

```java
// Query for a List of objects.
Query query = em.createQuery("Select e FROM Employee e WHERE e.salary > 100000");
List<Employee> result = query.getResultList();

// Query for a single object using a named parameter. The result is a single value.
// The named parameter is set using the query.setParameter() method.
Query query = em.createQuery("Select e FROM Employee e WHERE e.id = :id");
query.setParameter("id", id);
Employee result2 = (Employee)query.getSingleResult();

// Query for a single data element. The result is a single value.
Query query = em.createQuery("Select MAX(e.salary) FROM Employee e");
BigDecimal result3 = (BigDecimal)query.getSingleResult();

// Query for a List of data elements. The result is a List of Strings
Query query = em.createQuery("Select e.firstName FROM Employee e");
List<String> result4 = query.getResultList();

// Query for a List of element arrays. The result is a list of arrays.
Query query = em.createQuery("Select e.firstName, e.lastName FROM Employee e");
List<Object[]> result5 = query.getResultList();
```

####Positional Parameters in Queries
JPA defines named parameters and positional parameters. Named parameters can be specified in JPQL using the syntax :<name>. Positional parameters can be specified in JPQL using the syntax ? or ?<position>. Positional parameters start at position 1 not 0.

####Named parameter query example
```java
Query query = em.createQuery("SELECT e FROM Employee e WHERE e.firstName = :first and e.lastName = :last");
query.setParameter("first", "Bob");
query.setParameter("last", "Smith");
List<Employee> list = query.getResultList();
```

####Positional parameter query example
````java
Query query = em.createQuery("SELECT e FROM Employee e WHERE e.firstName = ? and e.lastName = ?");
query.setParameter(1, "Bob");
query.setParameter(2, "Smith");
List<Employee> list = query.getResultList();
````

####JPA Query with wildcards
What we are trying to do is get all the items that matches a pattern anywhere in their name.

The SQL query looks like this:
```
SELECT userName FROM Profile p WHERE p.userName LIKE %pattern%;
```

The JPQL query looks like this:
```java
SELECT p FROM Profile p WHERE p.userName LIKE ?1 ORDER BY p.userName ASC
```

I'm using annotations to create a named query.

@NamedQuery(name="Profile.getUsernameWithPattern", 
query="SELECT p FROM Profile p WHERE p.userName LIKE ?1 ORDER BY p.userName ASC")

Here's the code that demonstrates using this query:

Query query = strategy.getNamedQuery("Profile.getUsernameWithPattern");
query.setParameter(1, "%" + pattern + "%");        
query.getResultList();

 

