# SELECT

## Qëllimi

Marrja e të dhënave nga një tabelë.

---

## Të gjitha kolonat

```sql id="sql1a"
SELECT *
FROM customers;
```

---

## Kolona specifike

```sql id="sql1b"
SELECT customer_id, name, balance
FROM customers;
```

---

## Alias

```sql id="sql1c"
SELECT balance AS total_balance
FROM customers;
```

---

## SQL mindset

SELECT = "çfarë dua të shoh"

---

## Përdorime

- raportim
- analiza
- ETL fillestar