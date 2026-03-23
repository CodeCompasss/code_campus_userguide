# MySQL

### What is it?

MySQL is a professional-grade Relational Database Management System (RDBMS) based on Structured Query Language (SQL). It is a persistent storage engine that organizes data into structured tables with predefined relationships, ensuring data integrity through a set of rules known as ACID (Atomicity, Consistency, Isolation, Durability) properties.

In the software development ecosystem, MySQL belongs to the **persistence and data management layer**. It is one of the most widely deployed database engines in the world, powering everything from small personal blogs to massive, high-traffic web platforms.

### Installation (Optional)

!!! note
    CodeCampus OS includes MySQL (MariaDB) by default.
    Use the commands below only if you are installing it on a different Linux distribution.

=== "Arch / Manjaro"
    ```bash
    sudo pacman -S mariadb
    sudo mariadb-install-db --user=mysql --basedir=/usr --datadir=/var/lib/mysql
    sudo systemctl enable --now mariadb
    ```

=== "Ubuntu / Debian"
    ```bash
    sudo apt update
    sudo apt install mysql-server
    sudo systemctl enable --now mysql
    ```

=== "Fedora"
    ```bash
    sudo dnf install community-mysql-server
    sudo systemctl enable --now mysqld
    ```

### Why this tool matters (In Depth)

Most modern applications are "ephemeral"—their memory is cleared every time the program restarts. To build anything useful (like a user account system, a financial ledger, or a content management system), you need a way to store information that persists across restarts and system failures. MySQL matters because it provides **highly scalable, structured persistence**.

Unlike simple file-based storage, MySQL allows for complex queries that can filter through millions of records in milliseconds. Its "relational" nature means you can define links between different types of data (e.g., linking a "User" to their "Orders") without duplicating information, leading to highly efficient use of storage. Furthermore, MySQL is designed for **concurrency**, meaning hundreds of users can read and write to the database simultaneously without the data becoming corrupted—a task that is nearly impossible with standard text files.

For students, MySQL is the gateway to understanding "Backend Engineering." Learning to design schemas and write efficient SQL queries is a fundamental skill that applies to almost every specialized field in software development, from web development to data science.

### How students will actually use it

Students will use MySQL to build the data backends for their applications:

*   **Schema Design:** Creating tables with specific column types (e.g., `INT`, `VARCHAR`, `DATETIME`) and defining Primary Keys to uniquely identify records.
*   **Data Manipulation:** Performing CRUD (Create, Read, Update, Delete) operations using SQL commands like `INSERT INTO`, `SELECT`, and `UPDATE`.
*   **Relational Mapping:** Using "Foreign Keys" to build relationships between tables, such as connecting students to the courses they are enrolled in.
*   **Indexing for Speed:** Creating "Indexes" on frequently searched columns to ensure that their application remains fast as the amount of data grows.
*   **CLI Administration:** Using the `mysql` terminal client to manage users, grant permissions, and perform manual data audits.
