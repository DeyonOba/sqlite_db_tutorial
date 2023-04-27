# Sqlite Tutorial and Practice

The aim of this project is to read and practice the sqlite documentation with projects.

## Tutorial

The tutorial information can be found on the official documentation of python for [sqlite3](https://docs.python.org/3/library/sqlite3.html).

The tutorial a database of Monty Python Movies would be created using basic sqlite3 functionality. 

Fundamental concept need to successfully understand the project are the fundementals of cursors and transactions.

From [Wikipedia](https://en.wikipedia.org/wiki/Cursor_(databases)):
**Cursor (Databases)**
> A database cursor is a machanism that enables traversal over the records in a database. Cursors facilitate subsequent processing in conjunction with the traversal, such as retrieval, addition and removal of database records.

**Usage**
To use cursors in SQL procedure, you need to do the following:
1. Declare a cursor that defines a result set.
2. Open the cursor to establish the result set.
3. Fetch the data in local variable as needed from the cursor, one row at a time.
4. Close the cursor when done.

From [Wikipedia](https://en.wikipedia.org/wiki/Database_transaction): **Database Transaction**

> A database transaction symbolizes a unit of work, performed within a database management system against a database, that is treated in coherent and reliable way independent of other transactions. In a database management system, a transaction is a single unit of logic or work, sometimes made up of multiple operations. Any logical calculation done in a consistent mode in a database is known as a transaction.

A transaction generally represents any change in a database.Transactions in a database environment have two main purposes:

1. To provide reliable unites of work that allow correct recovey from failures and keep a database consistent even in cases of system failure.
2. To provide isolation between programs accessing a database concurrently. If this isolation is not provided, the programs outcomes are posibly erroneous.

Back to the sqlite tutorial from python documentation.

The first thing we would need to do is create a database that is connected to sqlite3. To do that we call on `sqlite3.connect()` to create a connection to the database `tutoraial.db` which is found in our current working directory,implicitly creating the database if it does not exist.

```python
import sqlite3
con = sqlite3. connect("tutorial.db")
```
