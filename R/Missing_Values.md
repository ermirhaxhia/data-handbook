# Missing Values

## Qëllimi

Trajtimi i vlerave mungesë.

---

## Kontroll

```r id="r6a"
sum(is.na(df))
```

---

## Filter NA

```r id="r6b"
df %>%
  filter(!is.na(balance))
```

---

## Zëvendësim

```r id="r6c"
df$balance[is.na(df$balance)] <- 0
```

---

## Me dplyr

```r id="r6d"
library(tidyr)

df %>%
  replace_na(list(balance = 0))
```

---

## SQL Equivalent

```sql id="r6e"
COALESCE(balance, 0)
```