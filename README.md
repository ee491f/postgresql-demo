# PostgreSQL Demo
A demonstration of the PostgreSQL material for [EE491F](https://ee491f.github.io/course-material/#postgresql "EE491F Course Webpage").  
Accompanying Videos: [https://youtu.be/YlK2QTsSPoQ](https://youtu.be/YlK2QTsSPoQ "Getting Started with PosgreSQL")

Outline
-------
1. Set Up PostgreSQL Container
1. Connect To PostgreSQL Database
    ```
    psql --host=database --username=unicorn_user --dbname=rainbow_database
    ```
1. Create a Table
1. Perform CRUD Operations
    * Read: `SELECT * FROM color_table;`
    * Create: `INSERT INTO color_table VALUES (‘pink’);`
    * Update: `UPDATE color_table SET name='hot pink' WHERE name = 'pink';`
    * Delete: `DELETE FROM color_table WHERE name = ‘hot pink’;`
1. Perform JOIN
    ```
    ALTER TABLE color_table ADD pony_name TEXT;
    CREATE TABLE pony_table (name TEXT, skill TEXT);
    INSERT INTO color_table VALUES ('rainbow', ‘Rainbow Dash’);
    INSERT INTO color_table VALUES (‘purple, ’Twilight Sparkle’);
    INSERT INTO pony_table VALUES (’Twilight Sparkle’, ‘studious’);
    INSERT INTO pony_table VALUES (’Rainbow Dash’, ‘speed’);
    SELECT * FROM color_table JOIN pony_table ON pony_table.name = color_table.pony_name;
    ```
1. Persist Data
