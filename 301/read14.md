# Reading notes for class 14a & b
## 14a - DB Normalization
- DB normalization is a process used to organzie a database into tables and columns. 
- The main idea is that a table should be about a specific topic and only supporting topics included. 
- Identify salespeople in your organization
- List all customers your company calls upon to sell a product
- Identify which salespeople calls on specific customers
- By limiting a table to one purpoise you reduce the number of duplicate data contained within your database.
### Reasons for Database Normalization
- First is it minimize duplicate data, the second is to minimize or avoid data modification issues, and the third is to simplify queries.
- Like to see tables that have one purpose. Having the table serve many purposes introduces many of the challenges; namely, data duplication, data update issues, and incread effort to query data.
### Data Duplication and Modification Anomalies
- It increases storage and decrease performance
- It becomes more difficult to maintain data changes
- Insert Anomaly
- Update Anomaly
- Deletion Anomaly
- Search and Sort Issues
### Def of Database Normalization
- There are three common forms of database normalization: 1st, 2nd, 3rd normal form. Also abbreviated as 1NF, 2NF, and 3NF.
- First Normal Form - The information is stored in a relational table with each column contianing atomic values. There a re no repeating groups of columns.
- Second Normal Form - The table is in first normal and all the columns depend on the tavle's primary key
- Third NOrmal Form - The is in second normal kform and all of its columns are not transitively dependent on the primary key.
