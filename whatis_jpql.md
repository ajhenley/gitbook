###What is JPQL?

The Java Persistence query language defines queries for entities and their persistent state. The query language allows you to write portable queries that work for any database. An application dvelioped 

The query language uses the abstract persistence schemas of entities, including their relationships, for its data model and defines operators and expressions based on this data model. The scope of a query spans the abstract schemas of related entities that are packaged in the same persistence unit. The query language uses an SQL-like syntax to select objects or values based on entity abstract schema types and relationships among them.

 
Creating Queries Using the Java Persistence Query Language

 

The EntityManager.createQuery and EntityManager.createNamedQuery methods are used to query the datastore by using Java Persistence query language queries.

The createQuery method is used to create dynamic queries, which are queries defined directly within an application’s business logic:

public List findWithName(String name) {
return em.createQuery(
    "SELECT c FROM Customer c WHERE c.name LIKE :custName")
    .setParameter("custName", name)
    .setMaxResults(10)
    .getResultList();
}

The createNamedQuery method is used to create static queries, or queries that are defined in metadata by using the javax.persistence.NamedQueryannotation. The name element of @NamedQuery specifies the name of the query that will be used with the createNamedQuery method. The query element of@NamedQuery is the query:

@NamedQuery(
    name="findAllCustomersWithName",
    query="SELECT c FROM Customer c WHERE c.name LIKE :custName"
)

Here’s an example of createNamedQuery, which uses the @NamedQuery:

@PersistenceContext
public EntityManager em;
...
customers = em.createNamedQuery("findAllCustomersWithName")
    .setParameter("custName", "Smith")
    .getResultList();

Named Parameters in Queries

Named parameters are query parameters that are prefixed with a colon (:). Named parameters in a query are bound to an argument by the following method:

javax.persistence.Query.setParameter(String name, Object value)

In the following example, the name argument to the findWithName business method is bound to the :custName named parameter in the query by callingQuery.setParameter:

public List findWithName(String name) {
    return em.createQuery(
        "SELECT c FROM Customer c WHERE c.name LIKE :custName")
        .setParameter("custName", name)
        .getResultList();
}

Named parameters are case-sensitive and may be used by both dynamic and static queries.

 
Positional Parameters in Queries

You may use positional parameters instead of named parameters in queries. Positional parameters are prefixed with a question mark (?) followed the numeric position of the parameter in the query. The Query.setParameter(integer position, Object value) method is used to set the parameter values.

In the following example, the findWithName business method is rewritten to use input parameters:

public List findWithName(String name) {
    return em.createQuery(
        “SELECT c FROM Customer c WHERE c.name LIKE ?1”)
        .setParameter(1, name)
        .getResultList();
}

Input parameters are numbered starting from 1. Input parameters are case-sensitive, and may be used by both dynamic and static queries.

 

 

 
JPA Query with wildcards

What we are trying to do is get all the items that matches a pattern anywhere in their name.

In simple SQL, what you want to do is:

 SELECT userName FROM Profile p WHERE p.userName LIKE %pattern%;

 I'm using annotations to create a named query.

@NamedQuery(name="Profile.getUsernameWithPattern", 
query="SELECT p FROM Profile p WHERE p.userName LIKE ?1 ORDER BY p.userName ASC")

(This will even sort the result!!)

Here's the code that demonstrates using this query:

 
Query query = strategy.getNamedQuery("Profile.getUsernameWithPattern");
query.setParameter(1, "%" + pattern + "%");        
 query.getResultList();

 

 An example of using multiple named queries....

@NamedQueries({
  @NamedQuery(name="Professor.findAll",
              query="SELECT e FROM Professor e"),
  @NamedQuery(name="Professor.findByPrimaryKey",
              query="SELECT e FROM Professor e WHERE e.id = :id"),
  @NamedQuery(name="Professor.findByName",
              query="SELECT e FROM Professor e WHERE e.name = :name")
