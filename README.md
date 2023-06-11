# Ex-09:
##  Implementation of ROLLUP in SQL
### AIM:
To create a SQL program by implementing of rollup.
### ALGORITHM:
1. Create a sample table in SQL using CREATE TABLE syntax
2. Insert all the values and Titles respectively using INSERT INTO syntax
3. Now check whether all the rows are affected or not by fetching the table
4. After checking, now use SELECT for choosing the column name that we want and use FROM to choose the table
5. Then use ROLLUP syntax for obtaining it's function.The ROLLUP in MySQL is a modifier used to produce the summary output, including extra rows that represent super-aggregate (higher-level) summary operations
6. After compiling and running the program, the results will be displayed.
### PROGRAM:
```sql
CREATE TABLE employee (
  Name VARCHAR(255),
  Year INT,
  Product VARCHAR(255),
  Cost int
);

INSERT INTO employee (Name, Year, Product, Cost) VALUES
  ('John', 2020, 'Micro oven', 10000),
  ('Jane', 2021, 'Laptop', 72000),
  ('Jane', 2019, 'Fridge', 80000),
  ('Michael', 2022, 'Cloth_organizer', 2000),
  ('Michael', 2021, 'Min Vacum', 900),
  ('Daniel', 2020, 'Led lights', 250),
  ('Daniel', 2023, 'Vacum cleaner', 2500),
  ('Daniel', 2022, 'Slicer', 200),
  ('Andrew', 2019, 'Mixer', 3000),
  ('Andrew', 2023, 'Air frier', 4000);
  
select year, sum(Cost) as Total_Sale from employee
group by year with rollup;
```
### OUTPUT:
![1](https://github.com/KeerthikaNagarajan/EX-09-SQL/assets/93427089/95b9656b-8d27-49cf-b09f-4b7679998990)

### RESULT:
Thus we have successfully obtained the required result using the above-given code.
