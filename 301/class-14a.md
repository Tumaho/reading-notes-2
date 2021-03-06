## Database Normalization

### What's Database Normalization?!

* **Database normalization** is a process used to **organize a database** into tables and columns.  The main idea with this is that a ***table should be about a specific topic and only supporting topics included***.

* By **limiting** a table to **one purpose** you ***reduce the number of duplicate data contained within your database***. This eliminates some issues stemming from database modifications.

### What is a Database Table?

* A **relational database** is made up of **several components**, of which the **table** is most significant. ***The database table is where all the data in a database is stored**, and without tables, there would not be much use for relational databases.

* Each row in a relational is uniquely  identified by a primary key.  This can be by one or more sets of column values.  In most scenarios it is a single column, such as employeeID.

* **Every relational table has one primary key**.  Its **purpose** is to uniquely identify each row in the database.  No two rows can have the same primary key value.  The practical result of this is that you can select every single row by just knowing its primary key.

* Columns are defined to hold a specific type of data, such as dates, numeric, or textual data.  In the simplest of definitions a column is defined by its name and data type.  The name is used in SQL statements when selecting and ordering data, and the data type is used to validate information stored.

* A table can contain zero or more rows.  When there are zero, it said to be empty.  There is not practical limit on the number of rows a table can hold.

* There is no guarantee that the rows in a table are stored in a particular order.  Use the `ORDER BY` clause to do so.

* Also, strictly speaking, in a relational database there is no first or last row.  Yes, you can tease out a first row of a result using a keyword such as LIMIT or TOP, but those are used once the data is retrieved and sorted.  The difference here is that you’re seeing the first row of the result, not what is physically stored in the table.

* In summary, you can think of the columns as giving the table its personality and the rows its substance.

* There are **three main reasons to normalize a database**:
  1. Minimize duplicate data
     * Duplicated information presents two problems:
       1. It increases storage and decrease performance.
       2. It becomes more difficult to maintain data changes.
  2. Minimize or avoid data modification issues
  3. Simplify queries. 

* There are three common forms of database normalization: **1st, 2nd, and 3rd normal form**. They are also abbreviated as **1NF, 2NF, and 3NF respectively**. 

* The forms are progressive, meaning that to qualify for 3rd normal form a table must first satisfy the rules for 2nd normal form, and 2nd normal form must adhere to those for 1st normal form.

* **First Normal Form** – The information is stored in a relational table with each column containing atomic values. There are no repeating groups of columns.

* **Second Normal Form** – The table is in first normal form and all the columns depend on the table’s primary key.

* **Third Normal Form** – the table is in second normal form and all of its columns are not transitively dependent on the primary key