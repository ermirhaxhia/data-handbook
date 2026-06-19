# Sorting Data

## Qëllimi

Renditja e të dhënave sipas një ose më shumë kolonave.

---

## Ascending

```python
df.sort_values("balance")
```

---

## Descending

```python
df.sort_values("balance", ascending=False)
```

---

## Shumë kolona

```python
df.sort_values(
    ["city", "balance"],
    ascending=[True, False]
)
```

---

## Ruajtja e ndryshimit

```python
df = df.sort_values("balance")
```

ose

```python
df.sort_values(
    "balance",
    inplace=True
)
```

---

## Top N

```python
df.sort_values(
    "balance",
    ascending=False
).head(10)
```

---

## SQL Equivalent

```sql
SELECT *
FROM customers
ORDER BY balance DESC;
```

---

## Përdorime tipike

- Top klientët
- Top degët
- Raporte financiare
- KPI ranking