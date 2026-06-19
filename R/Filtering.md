# Filtering in R

## Qëllimi

Përzgjedhja e rreshtave sipas kushteve.

---

## Base R

```r id="r2a"
df[df$balance > 0, ]
```

---

## dplyr (standard në industri)

```r id="r2b"
library(dplyr)

df %>%
  filter(balance > 0)
```

---

## Shumë kushte

```r id="r2c"
df %>%
  filter(city == "Tirana", balance > 0)
```

---

## OR condition

```r id="r2d"
df %>%
  filter(city == "Tirana" | city == "Durres")
```

---

## IN operator

```r id="r2e"
df %>%
  filter(city %in% c("Tirana", "Durres"))
```

---

## SQL Equivalent

```sql id="r2f"
SELECT *
FROM customers
WHERE balance > 0;
```

---

## Përdorime

- filtrimi i klientëve aktivë
- analiza risku
- clean data