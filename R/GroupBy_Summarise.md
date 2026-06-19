# Group By & Summarise

## Qëllimi

Agregim i të dhënave sipas grupeve.

---

## SUM

```r id="r4a"
df %>%
  group_by(city) %>%
  summarise(total_balance = sum(balance))
```

---

## COUNT

```r id="r4b"
df %>%
  group_by(city) %>%
  summarise(count = n())
```

---

## AVG

```r id="r4c"
df %>%
  group_by(city) %>%
  summarise(avg_balance = mean(balance))
```

---

## Shumë agregime

```r id="r4d"
df %>%
  group_by(city) %>%
  summarise(
    total = sum(balance),
    avg = mean(balance),
    n = n()
  )
```

---

## SQL Equivalent

```sql id="r4e"
SELECT city,
       SUM(balance),
       AVG(balance),
       COUNT(*)
FROM customers
GROUP BY city;
```

---

## Përdorime

- KPI raportim
- analiza rajonale
- banking analytics