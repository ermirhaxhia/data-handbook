# Advanced Excel Formulas

## 🎯 Qëllimi
Analiza dhe lookup në nivel profesional.

---

## 🔎 VLOOKUP
```excel
VLOOKUP(lookup_value, table_array, col_index, FALSE)
```

```excel
=VLOOKUP(A2,Customers!A:D,3,FALSE)
```

---

## 🔎 XLOOKUP
```excel
=XLOOKUP(A2,Customers!A:A,Customers!C:C)
```

---

## 🧠 INDEX + MATCH
```excel
=INDEX(C:C, MATCH(A2,A:A,0))
```

---

## 📊 SUMIFS
```excel
SUMIFS(sum_range, criteria_range1, criteria1)
```

```excel
=SUMIFS(C:C,A:A,"Tirana",B:B,">0")
```

---

## 📊 COUNTIFS
```excel
COUNTIFS(criteria_range1, criteria1)
```

```excel
=COUNTIFS(A:A,"Tirana",B:B,">0")
```

---

## 📊 AVERAGEIFS
```excel
AVERAGEIFS(avg_range, criteria_range1, criteria1)
```

```excel
=AVERAGEIFS(B:B,A:A,"Tirana")
```

---

## 🧠 IFERROR
```excel
IFERROR(value, value_if_error)
```

```excel
=IFERROR(VLOOKUP(A2,Table,2,FALSE),"Not Found")
```

---

## 🧠 IFNA
```excel
IFNA(value, value_if_na)
```

---

## 🔥 CHOOSE
```excel
CHOOSE(index_num, value1, value2, ...)
```

---

## 🔥 OFFSET
```excel
OFFSET(reference, rows, cols)
```

---

## 📊 MATCH
```excel
MATCH(lookup_value, lookup_array, 0)
```

---

## 💡 Use Case

- banking dashboards
- customer segmentation
- KPI reporting
- reconciliation