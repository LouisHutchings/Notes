# CS258 Database Systems lecture 2
*4/10/2018*

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
