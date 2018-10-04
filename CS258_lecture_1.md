# CS258 Database Systems lecture 1
*2/10/2018*

### What are the principal functions of a database system?
> DB systems provide software to manage data

A DB system can viewed as a black box which provides an interface for the following functionality:
* **Model** data
* **Access** data - query and update
* **Analyze** data - complex queries
* **Store** data
* **Secure** data
* **Consistent** data - data is maintained through failure and concurrent transactions
* **Optimize** data - use indicies and execute a set of data operators in the best order

### The Three Schema Architecture for DB management systems

> DB management systems == DB systems

1. **External level** - supports multiple views of the database for each user group
1. **Conceptual level** - hides physical details and shows database entities, data types, relations, operations, etc.
1. **Internal level** - describes the physical storage structure i.e data storage and access paths

### Data
Data can be classified as either **structured** (e.g tables with predefined columns) or **unstructured** (e.g web pages, text files).
Some data is **semi-structured**(XML or JSON based).

Database management systems were designed for structured data,, unstructured data was the domain of [information retrieval (IR)](https://en.wikipedia.org/wiki/Information_retrieval), however nowadays they can also handle many forms of unstructured data.

Data is often **too big** too fit in memory. This data is stored across many disks, typically spanning many computers in computer clusters or on disk farms.

Data is **decentralized**

### Data Modelling
In order to best model data it is important to know:
* What are the **data items** that need to be known
* What are the data items **attributes**
* What are the **relationships** between data items

### The Relational DB Model
> a database structured to recognize relations between stored items of information.

**informal definition:** A **relation is a table** with the following properties:
* A set of **rows**. The data elements in each row represent certain facts that correspond to a real-world entity or relation
  * in the formal model rows are called **tuples**
* Each column has a **column header** that indicates the meaning of the data elements in that column
  * in the formal model a column header is called an **attribute name**, or just **attribute**.
* A **key**. Each row must be uniquely identifiable.
  * row-ids or sequential numbers can be assigned as keys, called artificial or surrogate  keys

### Formal definitions for the relational database model

The **Schema** of a relation is denoted by R(A1,A2,......,AN) where R is the name of the relation and the attributes of the relation are A1,A2,...,AN.

Every attribute has a **domain**, a set of valid values. A domain has a logical definiton in the real world and a data format. The attribute name designates the role played by a domain in a relation.

A **tuple** is an ordered set of values (enclosed in angled brackets ‘< … >’). Each value is derived from an appropriate domain.

A **relation** is a set of tuples.

The relation **state** is a subset of the Cartesian product of the domains of its attributes.

A **database** is a collection of relations. A **database schema** is a set of all relational schemas in a database.

### Why the relational database model?
* It's **simple**.
* It's an **abstract model** but has been enriched with declrative programming laguages such as SQL.
* The abstract relational model is **set-oriented**. (SQL is based on "bags"(multisets), sets are not the same as bags).

### Relational database constrains
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
