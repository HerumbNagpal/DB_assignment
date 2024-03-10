1. Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.
Ans. The "category_id" column in the "Product" table likely serves as a foreign key referencing the "ID" column in the "Product_Category" table, establishing a relationship between products and their categories.


2. How could you ensure that each product in the "Product" table has a valid category assigned to it?
Ans. To ensure that each product in the "Product" table has a valid category assigned to it, we can use a foreign key constraint.
     For example :
     CREATE TABLE Product (
      id INT PRIMARY KEY,
      name VARCHAR(255),
      description TEXT,
      category_id INT,
      inventory_id INT,
      price DECIMAL(10, 2),
      discount_id INT,
      FOREIGN KEY (category_id) REFERENCES Product_Category(id)
      );
