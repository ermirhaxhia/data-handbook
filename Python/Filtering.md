# Filtering Data

## Qëllimi

Përzgjedhja e rreshtave sipas kushteve.

---

## Dataset Shembull

| customer_id | city   | balance |
|-------------|---------|----------|
| 1           | Tirana  | 1000     |
| 2           | Durres  | -200     |
| 3           | Tirana  | 500      |

---

## Filter i thjeshtë

```python
df[df["balance"] > 0]
```

Kthen vetëm klientët me balance pozitive.

---

## Disa kushte

```python
df[(df["city"] == "Tirana") & (df["balance"] > 0)]
```

---

## OR

```python
df[(df["city"] == "Tirana") | (df["city"] == "Durres")]
```

---

## IN

```python
df[df["city"].isin(["Tirana", "Durres"])]
```

---

## NOT IN

```python
df[~df["city"].isin(["Tirana", "Durres"])]
```

---

## NULL Values

```python
df[df["balance"].isna()]
```

```python
df[df["balance"].notna()]
```

---

## SQL Equivalent

```sql
SELECT *
FROM customers
WHERE balance > 0;
```

---

## Përdorime tipike

- Klientë aktivë
- Filtrim transaksionesh
- Kontroll gabimesh
- Përgatitje raportesh

---

## Gabime të zakonshme

❌

```python
df["balance"] > 0 and df["city"] == "Tirana"
```

✔

```python
(df["balance"] > 0) & (df["city"] == "Tirana")
```