# Datetime

## Qëllimi

Punimi me data dhe kohë.

---

## Konvertim në datetime

```python
df["date"] = pd.to_datetime(
    df["date"]
)
```

---

## Viti

```python
df["date"].dt.year
```

---

## Muaji

```python
df["date"].dt.month
```

---

## Dita

```python
df["date"].dt.day
```

---

## Emri i muajit

```python
df["date"].dt.month_name()
```

---

## Filtrim sipas datës

```python
df[
    df["date"] >= "2025-01-01"
]
```

---

## Diferenca mes datave

```python
df["days"] = (
    df["end_date"]
    -
    df["start_date"]
).dt.days
```

---

## SQL Equivalent

```sql
YEAR(date_column)

MONTH(date_column)

DATEDIFF(day,start,end)
```

---

## Përdorime tipike

- Raporte mujore
- Time series
- Analizë transaksionesh
- KPI sipas periudhës