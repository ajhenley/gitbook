###JPA Database Utilities

Make a class out of the following code to insert and update from the database.

 


import java.util.List;
import javax.persistence.EntityManager;
import javax.persistence.EntityTransaction;
import javax.persistence.NoResultException;
import javax.persistence.TypedQuery;

 

public class CustomerDB {

public static void insert(Customer customer) {
EntityManager em = DBUtil.getEmFactory().createEntityManager();
EntityTransaction trans = em.getTransaction();
trans.begin();
try {
em.persist(user);
trans.commit();
} catch (Exception e) {
System.out.println(e);
trans.rollback();
} finally {
em.close();
}
}

public static void update(Customer customer) {
EntityManager em = DBUtil.getEmFactory().createEntityManager();
EntityTransaction trans = em.getTransaction();
trans.begin();
try {
em.merge(user);
trans.commit();
} catch (Exception e) {
System.out.println(e);
trans.rollback();
} finally {
em.close();
}
}

public static void delete(Customer customer) {
EntityManager em = DBUtil.getEmFactory().createEntityManager();
EntityTransaction trans = em.getTransaction();
trans.begin();
try {
em.remove(em.merge(user));
trans.commit();
} catch (Exception e) {
System.out.println(e);
trans.rollback();
} finally {
em.close();
}
}
} 
