# Customer Report (Banking Use Case)

## 🎯 Qëllimi

Të krijojmë një raport për klientët aktivë të bankës:

- Total balance për klient
- Numër llogarish
- Status (active/inactive)
- Segment sipas qytetit

---

## 📂 Input Data

### customers

| customer_id | name | city   |
|------------|------|--------|
| 1          | Ana  | Tirana |
| 2          | Beni | Durres |
| 3          | Era  | Tirana |

---

### accounts

| account_id | customer_id | balance | status  |
|------------|-------------|---------|---------|
| 101        | 1           | 1000    | active  |
| 102        | 1           | 500     | active  |
| 103        | 2           | -200    | inactive|

---

## 🐍 Python Solution (pandas)

```python id="ex1a"
import pandas as pd

customers = pd.read_csv("customers.csv")
accounts = pd.read_csv("accounts.csv")

# 1. Merge datasets
df = pd.merge(customers, accounts, on="customer_id")

# 2. Aggregate per customer
report = df.groupby(["customer_id", "name", "city"]).agg(
    total_balance=("balance", "sum"),
    num_accounts=("account_id", "count")
).reset_index()

# 3. Create status flag
report["risk"] = report["total_balance"].apply(
    lambda x: "HIGH" if x < 0 else "LOW"
)

print(report)
```

---

## 🗄 SQL Solution

```sql id="ex1b"
SELECT
    c.customer_id,
    c.name,
    c.city,
    SUM(a.balance) AS total_balance,
    COUNT(a.account_id) AS num_accounts
FROM customers c
JOIN accounts a
ON c.customer_id = a.customer_id
GROUP BY c.customer_id, c.name, c.city;
```

---

## 💡 Business Insight

- Klientët me balance negative janë risk
- Tirana ka më shumë klientë → target marketing
- Numri i llogarive tregon aktivitetin e klientit

---

## 🧠 Çfarë tregon kjo në intervistë

- SQL JOIN + GROUP BY
- pandas merge + groupby
- logjikë biznesi (jo vetëm kod)