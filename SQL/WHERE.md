# WHERE

## Qëllimi

Filtrimi i rreshtave.

---

## Kusht i thjeshtë

```sql id="sql2a"
SELECT *
FROM customers
WHERE balance > 0;
```

---

## Shumë kushte

```sql id="sql2b"
SELECT *
FROM customers
WHERE balance > 0
  AND city = 'Tirana';
```

---

## OR

```sql id="sql2c"
WHERE city = 'Tirana'
   OR city = 'Durres';
```

---

## IN

```sql id="sql2d"
WHERE city IN ('Tirana', 'Durres');
```

---

## SQL mindset

WHERE = "cilat rreshta dua"