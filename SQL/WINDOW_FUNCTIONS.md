# Window Functions

## Qëllimi

Analizë pa humbur rreshtat individualë.

---

## Rank

```sql id="sql8a"
SELECT *,
       RANK() OVER (ORDER BY balance DESC) AS rank
FROM customers;
```

---

## Partition

```sql id="sql8b"
SELECT *,
       RANK() OVER (
           PARTITION BY city
           ORDER BY balance DESC
       ) AS city_rank
FROM customers;
```

---

## Running total

```sql id="sql8c"
SELECT *,
       SUM(balance) OVER (
           ORDER BY customer_id
       ) AS running_total
FROM customers;
```

---

## SQL mindset

Window functions = "analytics pa GROUP BY"