# Merge

## Qëllimi

Bashkimi i tabelave.

---

## Dataset

Customers

| customer_id | name |
|------------|------|
| 1 | Ana |
| 2 | Beni |

Accounts

| customer_id | balance |
|------------|---------|
| 1 | 1000 |
| 2 | 500 |

---

## Inner Join

```python
pd.merge(customers,
         accounts,
         on="customer_id")
```

---

## Left Join

```python
pd.merge(customers,
         accounts,
         on="customer_id",
         how="left")
```

---

## Right Join

```python
pd.merge(customers,
         accounts,
         on="customer_id",
         how="right")
```

---

## Full Join

```python
pd.merge(customers,
         accounts,
         on="customer_id",
         how="outer")
```

---

## SQL Equivalent

```sql
SELECT *
FROM customers c
INNER JOIN accounts a
ON c.customer_id = a.customer_id;
```

---

## Përdorime tipike

- Klient + kredi
- Klient + transaksione
- Bashkim raportesh