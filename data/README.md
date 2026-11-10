# Sample data

A small, fully synthetic DuckDB database built by a seeded script (planned: `build_db.py`), so everyone gets identical data and expected answers stay stable. The generated `.duckdb` file is not committed.

Planned tables: customers, products, orders (with a cancelled status), and an `orders_staging` table. Planned traps: cancelled orders, an unvalidated staging table, and two metrics that both match "revenue".
