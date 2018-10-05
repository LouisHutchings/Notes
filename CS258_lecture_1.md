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
