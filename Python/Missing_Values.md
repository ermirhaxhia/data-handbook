# Missing Values

## Kontroll

```python
df.isna().sum()
```

---

## Rreshtat me NULL

```python
df[df["balance"].isna()]
```

---

## Fshirje

```python
df.dropna()
```

---

## Zëvendësim

```python
df["balance"].fillna(0)
```

---

## Mesatare

```python
df["balance"].fillna(
    df["balance"].mean()
)
```

---

## SQL Equivalent

```sql
COALESCE(balance,0)
```