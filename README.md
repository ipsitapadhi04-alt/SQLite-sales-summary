🧮  Basic Sales Summary using SQLite and Python

📘 Objective
The objective of this project is to connect a tiny SQLite database to Python, run basic SQL queries to retrieve simple sales insights (like total quantity sold and total revenue), and visualize the results using Matplotlib.

⚙️ Tools and Technologies Used
- **Python** (Core language)
- **SQLite3** (Built-in database, no external setup required)
- **Pandas** (For data handling and querying)
- **Matplotlib** (For basic visualization)

🧱 Dataset
A small SQLite database file `sales_data.db` is created within the script, containing a single table named **sales** with the following fields:
- `product` (TEXT)
- `quantity` (INTEGER)
- `price` (REAL)

🧠 SQL Query Used
```sql
SELECT 
    product, 
    SUM(quantity) AS total_qty, 
    SUM(quantity * price) AS revenue
FROM sales
GROUP BY product;
