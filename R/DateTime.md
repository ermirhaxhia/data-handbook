# Date & Time in R

## Qëllimi

Punimi me data.

---

## Konvertim

```r id="r7a"
df$date <- as.Date(df$date)
```

---

## Lubridate (shumë i përdorur)

```r id="r7b"
library(lubridate)

year(df$date)
month(df$date)
day(df$date)
```

---

## Filtrim

```r id="r7c"
df %>%
  filter(date >= as.Date("2025-01-01"))
```

---

## Diferenca

```r id="r7d"
df$diff <- as.numeric(df$end - df$start)
```

---

## Përdorime

- time series
- banking reports
- KPI mujore