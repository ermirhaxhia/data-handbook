# Sales Aggregation Report

## 🎯 Qëllimi

Analizë e shitjeve sipas:

- qytetit
- muajit
- produktit

---

## 📂 Input Data

| date       | city   | product | sales |
|------------|--------|---------|-------|
| 2025-01-01 | Tirana | Loan A  | 1000  |
| 2025-01-02 | Tirana | Loan B  | 500   |
| 2025-01-02 | Durres | Loan A  | 300   |

---

## 🐍 Python Solution

```python id="ex2a"
df["date"] = pd.to_datetime(df["date"])

df["month"] = df["date"].dt.month

sales_report = df.groupby(["city", "month"]).agg(
    total_sales=("sales", "sum"),
    avg_sales=("sales", "mean")
).reset_index()
```

---

## 🗄 SQL Solution

```sql id="ex2b"
SELECT
    city,
    MONTH(date) AS month,
    SUM(sales) AS total_sales,
    AVG(sales) AS avg_sales
FROM sales
GROUP BY city, MONTH(date);
```

---

## 📊 Insight

- Tirana ka volum më të madh
- Krahasim mujor tregon trend
- përdoret për KPI dashboard

---

## 🧠 Skills

- datetime handling
- groupby / aggregation
- business reporting