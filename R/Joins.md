# Joins in R

## Qëllimi

Bashkimi i dataset-eve.

---

## Inner Join

```r id="r5a"
df1 %>%
  inner_join(df2, by = "customer_id")
```

---

## Left Join

```r id="r5b"
df1 %>%
  left_join(df2, by = "customer_id")
```

---

## Right Join

```r id="r5c"
df1 %>%
  right_join(df2, by = "customer_id")
```

---

## Full Join

```r id="r5d"
df1 %>%
  full_join(df2, by = "customer_id")
```

---

## SQL Equivalent

```sql id="r5e"
SELECT *
FROM customers c
LEFT JOIN accounts a
ON c.customer_id = a.customer_id;
```

---

## Përdorime

- klient + kredi
- klient + transaksione