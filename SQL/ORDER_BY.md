# ORDER BY

## Qëllimi

Renditja e rezultateve.

---

## Ascending

```sql id="sql3a"
SELECT *
FROM customers
ORDER BY balance;
```

---

## Descending

```sql id="sql3b"
SELECT *
FROM customers
ORDER BY balance DESC;
```

---

## Shumë kolona

```sql id="sql3c"
ORDER BY city ASC, balance DESC;
```

---

## SQL mindset

ORDER BY = "si i shoh rezultatet"