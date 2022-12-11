## ATOMICITY

- All queries in a transaction must succeed.
- If one query fails, all prior successfull queries in the transaction should rollback.
- If the database went down prior to a commit of a transaction.
- All the successful queries in the transaction should rollback.

| ACCOUNT_ID | BALANCE |
| ---------- | ------- |
| 1          | 1000    |
| 2          | 500     |

Send 100 From Account 1 to Account 2

```SQL
BEGIN TX1
1. SELECT BALANCE FROM ACCOUNT WHERE ID = 1
2. BALANCE > 100
3. UPDATE ACCOUNT SET BALANCE = BALANCE - 100 WHERE ID = 1
------CRASH------
```

- After we restarted the machine the first account has been debited but the other account has not been credited.
- This is really bas as we lost data, and the information is inconsistent.
- An atomic transaction is a transaction that will rollback all queries if one or more queries failed.

### SUMMARY

Atomicity is the idea of Transaction being one unit of work and that can't be split.
