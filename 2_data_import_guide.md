# Data Import Methodology

To populate the `pizza_sales` table with raw transactional records efficiently, use the standard database bulk copy protocol or local infile management configurations:

```sql
BULK INSERT pizza_sales
FROM 'C:\PizzaSalesProject\pizza_sales_data.csv'
WITH (
    FIELDTERMINATOR = ',',
    ROWTERMINATOR = '\n',
    FIRSTROW = 2
);
