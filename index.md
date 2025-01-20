
## what is a transaction ?  
A Transaction is  a collection of queries that are treated as one unit.

## What is Atomicity ?
All queries in a transaction must succeed. If one query fails, all prior successful queries in the transaction
should rollback. If the database went down prior to a commit of a transaction,
all the successful queries in the transactions should rollback  

## Isolation

### Read uncomitted
any transaction can read uncomitted writes of any other transaction
### Read comitted
transaction can read ONLY comitted writes of any other transaction
### Repeatable reads
poses a lock on a record until the the transaction is comitted.
## Searlization
