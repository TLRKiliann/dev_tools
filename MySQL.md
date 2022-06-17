# MySQL

## Install

`└─ $ ▶ mysql -u root -p`

You will need to connect to some remote host.

`└─ $ ▶ mysql -u {USERNAME} -h {hostIP} -p`

## Create DataBase :

`CREATE DATABASE IF NOT EXISTS db_name;`

## Use DataBase :

`USE DATABASE db_name;`

## Create Table



```
CREATE TABLE `orders` (
  `order_id` INT NOT NULL,
  `customer_name` VARCHAR(255),
  `city` VARCHAR(255),
  `order_total` DECIMAL(5,2),
  `order_date` VARCHAR(255),
  PRIMARY KEY (order_id)
) 
```

---

## Show all databases :

`SHOW databases;`

## Delete DataBase :

`DROP db_name users;`

## Switch to a DataBase :

`USE db_name;`

---

## Show all Tables :

`SHOW TABLES;`

## Display field formats :

`DESC table_name;`

## Delete Table :

`DROP TABLE table_name;`

## All the filed names and type of a table in MySQL Command using the below query :

`DESC os_users;`

## Display total number of rows in a Table :

`SELECT* count(*) FROM table_name;`

## Insert data into Table :

```
INSERT INTO `product_details` 
(`product_id`,`product_name`) VALUES
(1,'Biscuits'),(2,'Chocolates');`
```

## Retrieve data from Tables :

```
INSERT INTO `product_details` 
(`product_id`,`product_name`) VALUES
(1,'Biscuits'),(2,'Chocolates');
```

## Show certain selected rows with the value “whatever”. 

`SELECT * FROM [table name] WHERE [field name] = “whatever”;`



---

## Join 2 Tables :

## Without joining really, just to display :

**For example :**

`SELECT * FROM tableA a, tableB b; `

### By column name :

```
SELECT column_name(s)
FROM table1 INNER JOIN table2
ON table1.column_name=table2.column_name;
```

### Another manner :

```
SELECT column_name(s)
FROM table1
JOIN table2
ON table1.column_name=table2.column_name;
```


