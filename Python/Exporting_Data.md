# Exporting Data

## Qëllimi

Ruajtja e rezultateve në formate të ndryshme.

---

## CSV

```python
df.to_csv(
    "output.csv",
    index=False
)
```

---

## Excel

```python
df.to_excel(
    "output.xlsx",
    index=False
)
```

---

## Excel me shumë sheets

```python
with pd.ExcelWriter(
    "report.xlsx"
) as writer:

    df1.to_excel(
        writer,
        sheet_name="Customers"
    )

    df2.to_excel(
        writer,
        sheet_name="Loans"
    )
```

---

## SQL Table

```python
df.to_sql(
    "customers",
    conn,
    if_exists="replace"
)
```

---

## JSON

```python
df.to_json(
    "output.json"
)
```

---

## Përdorime tipike

- Raporte financiare
- ETL
- Dashboard feeds
- Data exchange