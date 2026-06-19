# HAVING

## Qëllimi

Filtrim pas agregimit.

---

## Shembull

```sql id="sql5a"
SELECT city,
       SUM(balance)
FROM customers
GROUP BY city
HAVING SUM(balance) > 10000;
```

---

## Dallimi me WHERE

- WHERE → para GROUP BY
- HAVING → pas GROUP BY

---

## SQL mindset

HAVING = "filtrim i rezultateve të agreguara"