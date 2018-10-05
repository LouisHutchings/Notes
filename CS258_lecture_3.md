# CS258 Database Systems lecture 3
*?/10/2018*
### Why the relational database model?
* It's **simple**.
* It's an **abstract model** but has been enriched with declrative programming laguages such as SQL.
* The abstract relational model is **set-oriented**. (SQL is based on "bags"(multisets), sets are not the same as bags).

### Relational database constraints
There are three constraints for R-DBMs (excluding domain constraints).
1. **Key constraints**
  * Superkey of R: a subset of attributes of R, SK, such that in any valid state for r(R), for any two distinct tuples t1 and t2 in r(R), t1[SK] ≠ t2[SK]
  * Candidate key of R: a minimal superkey. Any key K is a "minimal" superkey if the removal of any attribute from K results in a set of attributes that is no longer a superkey.
  * If a relation has several candidate keys, one is chosen arbitrarily to be the primary key.
1. **Entity integrity** constraints
  * The primary key attributes PK cannot be NULL in any tuple of r(R).
  * Any attribute of R (even non-key) may be not allowed to be NULL
1. **Referential integrity** constraints
  * A set of attributes FK from relation R1 is a foreign key that references relation R2 if attribute(s) in FK from R1 have the same domain as the attribute(s) in the primary key PK of R2, and a value of FK in a tuple t1 of R1 either refers to a value of the PK of some tuple t2 in R2 Or is NULL.
