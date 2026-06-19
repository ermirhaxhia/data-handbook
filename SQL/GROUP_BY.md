# GROUP BY

## Qëllimi

Agregimi sipas kategorive.

---

## SUM

```sql id="sql4a"
SELECT city,
       SUM(balance)
FROM customers
GROUP BY city;
```

---

## COUNT

```sql id="sql4b"
SELECT city,
       COUNT(*)
FROM customers
GROUP BY city;
```

---

## AVG

```sql id="sql4c"
SELECT city,
       AVG(balance)
FROM customers
GROUP BY city;
```

---

## SQL mindset

GROUP BY = "grupim + KPI"