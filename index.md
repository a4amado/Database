
## what is a transaction ?  
A Transaction is  a collection of queries that are treated as one unit.

## What is Atomicity ?
All queries in a transaction must succeed. If one query fails, all prior successful queries in the transaction
should rollback. If the database went down prior to a commit of a transaction,
all the successful queries in the transactions should rollback  

## Isolation Levels in Databases:
### Read Uncommitted

Description: Transactions can read uncommitted changes (writes) made by other transactions.
Implication: This can lead to dirty reads, where a transaction sees data that might later be rolled back.
### Read Committed

Description: A transaction can only read data that has been committed by other transactions.
Implication: This prevents dirty reads, but non-repeatable reads (where the same query returns different results within the same transaction) can still occur.
### Repeatable Read

Description: Ensures that if a transaction reads a record, it will see the same value for that record throughout the transaction, even if other transactions modify it. This is typically achieved by placing a shared lock on the read data until the transaction completes.
Implication: Prevents dirty reads and non-repeatable reads, but phantom reads (new rows being added by other transactions) can still occur.

## Searlization
