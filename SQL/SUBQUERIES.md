# Subqueries

## Qëllimi

Query brenda query.

---

## Shembull

```sql id="sql7a"
SELECT *
FROM customers
WHERE balance > (
    SELECT AVG(balance)
    FROM customers
);
```

---

## IN subquery

```sql id="sql7b"
SELECT *
FROM customers
WHERE customer_id IN (
    SELECT customer_id
    FROM accounts
);
```

---

## SQL mindset

Subquery = "pyetje brenda pyetjes"