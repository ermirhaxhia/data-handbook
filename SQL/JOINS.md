# JOINS

## Qëllimi

Bashkimi i tabelave.

---

## INNER JOIN

```sql id="sql6a"
SELECT *
FROM customers c
JOIN accounts a
ON c.customer_id = a.customer_id;
```

---

## LEFT JOIN

```sql id="sql6b"
SELECT *
FROM customers c
LEFT JOIN accounts a
ON c.customer_id = a.customer_id;
```

---

## RIGHT JOIN

```sql id="sql6c"
RIGHT JOIN accounts a
ON c.customer_id = a.customer_id;
```

---

## FULL JOIN

```sql id="sql6d"
FULL JOIN accounts a
ON c.customer_id = a.customer_id;
```

---

## SQL mindset

JOIN = "lidhja e realiteteve të ndryshme të të dhënave"