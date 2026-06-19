# ETL Workflow (Banking Pipeline)

## 🎯 Qëllimi

Të simulojmë një pipeline real:

> Extract → Transform → Load → Report

---

## 🔵 1. Extract (marrja e të dhënave)

```python id="ex3a"
import pandas as pd

customers = pd.read_csv("customers.csv")
accounts = pd.read_csv("accounts.csv")
```

---

## 🟡 2. Transform (pastrimi + logjika)

```python id="ex3b"
df = pd.merge(customers, accounts, on="customer_id")

# remove missing values
df = df.dropna()

# create KPI
df["risk_flag"] = df["balance"].apply(
    lambda x: "HIGH" if x < 0 else "LOW"
)
```

---

## 🟢 3. Aggregation Layer

```python id="ex3c"
report = df.groupby("city").agg(
    total_balance=("balance", "sum"),
    num_customers=("customer_id", "nunique")
).reset_index()
```

---

## 🔴 4. Load (export)

```python id="ex3d"
report.to_excel("city_report.xlsx", index=False)
```

---

## 🗄 SQL Equivalent Pipeline

```sql id="ex3e"
-- Extract
SELECT *
FROM customers c
JOIN accounts a
ON c.customer_id = a.customer_id;

-- Transform + Aggregate
SELECT city,
       SUM(balance),
       COUNT(DISTINCT customer_id)
FROM data
GROUP BY city;
```

---

## 💡 Real Business Use

- Daily banking reports
- Risk analysis
- Regulatory reporting
- Management dashboards

---

## 🧠 Çfarë tregon kjo

- kuptim i ETL
- data pipeline thinking
- automatizim i proceseve reale