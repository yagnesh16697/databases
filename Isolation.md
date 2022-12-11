## ISOLATION

- Can my inflight transaction see change made by other transaction?

### Read phenomena

1. Dirty Reads

| PID       | QNT | PRICE |
| --------- | --- | ----- |
| Product 1 | 10  | 5     |
| Product 2 | 20  | 4     |

```SQL
BEGIN TX1                                   BEGIN TX2

1. SELECT PID,QNT*PRICE FROM SALES
      Product 1,50
      Product 2,80

                                            2. UPDATE SALES SET QNT = QNT + 5 WHERE PID = 1


3. SELECT SUM(QNT*PRICE) FROM SALES

    -- We get 155 when it should be 130
    -- We read a "dirty" value that has
    -- not beeN committed

COMMIT TX1                                  ROLLBACK TX2

```

2. Non-repeatable Reads

3. Phantom Reads

4. Lost Updates

Isolation Levels
