# Aggregations

## Qëllimi

Përmbledhja e të dhënave në vlera statistikore.

---

## SUM

```python
df["balance"].sum()
```

---

## COUNT

```python
df["customer_id"].count()
```

---

## MEAN

```python
df["balance"].mean()
```

---

## MIN

```python
df["balance"].min()
```

---

## MAX

```python
df["balance"].max()
```

---

## MEDIAN

```python
df["balance"].median()
```

---

## STD

```python
df["balance"].std()
```

---

## Shumë agregime

```python
df.agg({
    "balance": [
        "sum",
        "mean",
        "max"
    ]
})
```

---

## SQL Equivalent

```sql
SELECT
    SUM(balance),
    AVG(balance),
    MIN(balance),
    MAX(balance)
FROM customers;
```

---

## Përdorime tipike

- KPI
- Raporte mujore
- Financial reporting
- Kontroll cilësie të të dhënave