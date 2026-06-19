# Exporting Data in R

## CSV

```r id="r8a"
write.csv(df, "output.csv", row.names = FALSE)
```

---

## Excel

```r id="r8b"
library(writexl)

write_xlsx(df, "output.xlsx")
```

---

## Multiple sheets

```r id="r8c"
library(openxlsx)

write.xlsx(
  list(
    sheet1 = df1,
    sheet2 = df2
  ),
  "report.xlsx"
)
```

---

## SQL export

```r id="r8d"
library(DBI)

dbWriteTable(conn, "customers", df)
```

---

## Përdorime

- reporting
- ETL pipelines
- finance exports