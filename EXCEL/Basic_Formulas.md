# Basic Excel Formulas

## 🎯 Qëllimi
Operacionet bazë për analiza të shpejta dhe KPI.

---

## ➕ SUM
```excel
SUM(number1, [number2], ...)
```

### Shembull
```excel
=SUM(A1:A100)
```

### Use case
- total loans
- total deposits
- total revenue

---

## ➗ AVERAGE
```excel
AVERAGE(number1, ...)
```

```excel
=AVERAGE(B2:B100)
```

---

## 🔢 COUNT
```excel
COUNT(value1, ...)
```

```excel
=COUNT(A:A)
```

Numëron vetëm numerikët.

---

## 📄 COUNTA
```excel
COUNTA(value1, ...)
```

```excel
=COUNTA(A:A)
```

Numëron të gjitha jo-bosh.

---

## ❌ COUNTBLANK
```excel
=COUNTBLANK(A:A)
```

---

## 🧠 IF
```excel
IF(logical_test, value_if_true, value_if_false)
```

```excel
=IF(B2>0,"ACTIVE","INACTIVE")
```

---

## 🧠 Nested IF
```excel
=IF(B2>1000,"HIGH",IF(B2>0,"MEDIUM","LOW"))
```

---

## ⚖️ AND
```excel
AND(logical1, logical2, ...)
```

```excel
=IF(AND(B2>0,C2="Tirana"),"OK","NO")
```

---

## ⚖️ OR
```excel
OR(logical1, logical2)
```

```excel
=IF(OR(B2>0,C2="VIP"),"YES","NO")
```

---

## 🔁 NOT
```excel
NOT(logical)
```

```excel
=NOT(B2>0)
```

---

## 🔍 ISBLANK
```excel
=ISBLANK(A2)
```

---

## 💡 Use Case

- client classification
- risk flags
- KPI dashboards
- data validation