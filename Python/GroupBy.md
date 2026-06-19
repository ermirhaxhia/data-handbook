# GroupBy

## Qëllimi

Ndarja e të dhënave në grupe dhe aplikimi i agregimeve.

---

## SUM sipas qytetit

```python
df.groupby("city")["balance"].sum()
```

---

## COUNT sipas qytetit

```python
df.groupby("city")["customer_id"].count()
```

---

## MEAN sipas qytetit

```python
df.groupby("city")["balance"].mean()
```

---

## Shumë agregime

```python
df.groupby("city").agg({
    "balance": [
        "sum",
        "mean"
    ],
    "customer_id": "count"
})
```

---

## Grupim me disa kolona

```python
df.groupby(
    ["city", "gender"]
)["balance"].sum()
```

---

## SQL Equivalent

```sql
SELECT
    city,
    SUM(balance)
FROM customers
GROUP BY city;
```

---

## Përdorime tipike

- KPI sipas degës
- KPI sipas rajonit
- Analiza klientësh
- Raporte financiare