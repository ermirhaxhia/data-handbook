# Reading Data in R

## Qëllimi

Leximi i të dhënave nga burime të ndryshme.

---

## CSV

```r id="r1a"
df <- read.csv("customers.csv")
```

---

## Tidyverse (më modern)

```r id="r1b"
library(readr)

df <- read_csv("customers.csv")
```

---

## Excel

```r id="r1c"
library(readxl)

df <- read_excel("customers.xlsx")
```

---

## Kontroll fillestar

```r id="r1d"
head(df)
str(df)
summary(df)
```

---

## Përdorime

- ETL
- Analizë financiare
- Raporte