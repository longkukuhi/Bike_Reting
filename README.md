# Bike rental database notebook

This notebook sketches the SQLite data model for a bike rental service. It creates four tables in a local file named `bikeRenting.db`. The customer, bike, order and defect-management functions in the last cell are placeholders.

## Try the schema

Open [Bike_rent_database.ipynb](Bike_rent_database.ipynb) in Jupyter with a Python kernel and run the cells from top to bottom in a fresh directory. The notebook uses Python's built-in `sqlite3` module. Its `CREATE TABLE` statements expect a new database, so rerunning them against an existing file raises a “table already exists” error.

| Table | What it records |
| --- | --- |
| `CUSTOMERS` | Customer ID, name, phone, bank details and balance. The balance column is spelled `BANLANCE` in the schema. |
| `BIKE` | Bike ID, status and location. |
| `ORDER_ALL` | Customer and bike IDs, rental times, payment status and amount. |
| `REPORT` | Defect reports, including the bike, message, time and status. |

To inspect the result, run this in a new notebook cell. It lists the tables without changing the database.

```python
data.execute("SELECT name FROM sqlite_master WHERE type = 'table' ORDER BY name").fetchall()
```
