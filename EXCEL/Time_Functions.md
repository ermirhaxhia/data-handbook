# Time Functions in Excel

## 🎯 Qëllimi
Analizë kohore për banking & reporting.

---

## 📅 TODAY
```excel
=TODAY()
```

---

## ⏱ NOW
```excel
=NOW()
```

---

## 📆 YEAR
```excel
=YEAR(A2)
```

---

## 📆 MONTH
```excel
=MONTH(A2)
```

---

## 📆 DAY
```excel
=DAY(A2)
```

---

## 📆 WEEKDAY
```excel
=WEEKDAY(A2)
```

---

## 📆 TEXT date format
```excel
=TEXT(A2,"YYYY-MM")
```

---

## 📊 DATEDIF
```excel
DATEDIF(start_date, end_date, unit)
```

### Shembuj
```excel
=DATEDIF(A2,B2,"d")
=DATEDIF(A2,B2,"m")
=DATEDIF(A2,B2,"y")
```

---

## ⏳ EOMONTH
```excel
=EOMONTH(A2,0)
```

---

## 📈 WORKDAY
```excel
=WORKDAY(A2,10)
```

---

## 💡 Use Case

- loan maturity
- customer tenure
- monthly reporting
- risk exposure periods
