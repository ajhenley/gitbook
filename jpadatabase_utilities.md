# JPA Database Utilities

Make a class out of the following code to insert and update from the database.

 

 

import java.util.List;
import javax.persistence.EntityManager;
import javax.persistence.EntityTransaction;
import javax.persistence.NoResultException;
import javax.persistence.TypedQuery;

 

public class UserDB {

public static void insert(User user) {
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

public static void update(User user) {
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

public static void delete(User user) {
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