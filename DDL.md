- 数据库的创建（CREATE DATABASE语句）  

 模板：

``` CREATE DATABASE <数据库名称>;  ```

 样例：

``` CREATE DATABASE shop;  ```

- 表的创建（CREATE TABLE语句）  

  模板：

```SQL
CREATE TABLE <表名>
（<列名1> <数据类型> <该列所需约束>，
<列名2> <数据类型> <该列所需约束>，
<列名3> <数据类型> <该列所需约束>，
<列名4> <数据类型> <该列所需约束>，
.
.
.
<该表的约束1>， <该表的约束2>，……）；
```

  样例：

```SQL
CREATE TABLE Product
(product_id CHAR(4) NOT NULL,
product_name VARCHAR(100) NOT NULL,
product_type VARCHAR(32) NOT NULL,
sale_price INTEGER ,
purchase_price INTEGER ,
regist_date DATE ,
PRIMARY KEY (product_id));  
```

- 表的删除和更新  

  模板：  

  ```SQL
  DROP TABLE <表名>  
  ```

  样例：  

  ```SQL
  DROP TABLE Product;  
  ```

-   表定义的更新（ALTER TABLE语句）  

  模板：  

  ```sql
  ALTER TABLE <表名> ADD COLUMN <列的定义>；
  Oracle：ALTER TABLE <表名> ADD <列名> ；   
  ```

  样例：

  ```sql
  DB2 PostgreSQL MySQL
  ALTER TABLE Product ADD COLUMN product_name_pinyin VARCHAR(100);  
    Oracle
  ALTER TABLE Product ADD (product_name_pinyin VARCHAR2(100));  
  ```

-   删除列的ALTER TABLE语句  

  模板：  

  ```SQL
  ALTER TABLE <表名> DROP COLUMN <列名>；  
    Oracle中不用写COLUMN。
  ALTER TABLE <表名> DROP <列名> ； 
  ```

  样例：

  ```SQL
   SQL Server DB2 PostgreSQL MySQL
  ALTER TABLE Product DROP COLUMN product_name_pinyin;
  Oracle
  ALTER TABLE Product DROP (product_name_pinyin);  
  ```

- 插入数据

  ```SQL
  INSERT INTO Product VALUES ('0001', 'T恤衫', '衣服', 1000, 500, '2009-09-20');
  INSERT INTO Product VALUES ('0002', '打孔器', '办公用品', 500, 320, '2009-09-11');
  INSERT INTO Product VALUES ('0003', '运动T恤', '衣服', 4000, 2800, NULL);
  INSERT INTO Product VALUES ('0004', '菜刀', '厨房用具', 3000, 2800, '2009-09-20');
  INSERT INTO Product VALUES ('0005', '高压锅', '厨房用具', 6800, 5000, '2009-01-15');
  INSERT INTO Product VALUES ('0006', '叉子', '厨房用具', 500, NULL, '2009-09-20');
  INSERT INTO Product VALUES ('0007', '擦菜板', '厨房用具', 880, 790, '2008-04-28');
  INSERT INTO Product VALUES ('0008', '圆珠笔', '办公用品', 100, NULL,'2009-11-11');  
  ```

   

  

