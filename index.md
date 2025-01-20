
## what is a transaction ?  
A Transaction is  a collection of queries that are treated as one unit.

## What is Atomicity ?
All queries in a transaction must succeed. If one query fails, all prior successful queries in the transaction
should rollback. If the database went down prior to a commit of a transaction,
all the successful queries in the transactions should rollback  
