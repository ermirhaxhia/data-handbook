# Arrange (Sorting)

## Qëllimi

Renditja e të dhënave.

---

## Ascending

```r id="r3a"
df %>%
  arrange(balance)
```

---

## Descending

```r id="r3b"
df %>%
  arrange(desc(balance))
```

---

## Shumë kolona

```r id="r3c"
df %>%
  arrange(city, desc(balance))
```

---

## SQL Equivalent

```sql id="r3d"
SELECT *
FROM customers
ORDER BY balance DESC;
```

---

## Përdorime

- Top klientët
- Ranking
- Raporte financiare