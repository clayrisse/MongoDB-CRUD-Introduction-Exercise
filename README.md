# MongoDB | CRUD Operations

<br>

<img src="https://www.miltonmarketing.com/wp-content/uploads/2018/04/crudallprogramsdoitdownload.png" alt="img" style="zoom:33%;" />

<br>

## Create and query a collection - Exercise 1

<br>

### Getting Started

First, clone this repository as you will use it to import the data from the file`employees.json` to your MongoDB database.

```bash
# Clone the repository
git clone https://github.com/ross-u/MongoDB-CRUD-Introduction-Exercise.git

# Navigate to the directory of the exercise
cd  MongoDB-CRUD-Introduction-Exercise
```

<br>

In this exercise we are going to create a new database and a document `collection` inside of that database.

After the initial step of creating the database and the collection we will have a chance to get a hand on using the basic MongoDB queries in the `mongo` shell.

<br>

<hr>

**Task 1 :**

We will first create the database called `ironhack-inc` and then create a new collection named `employees` inside it.

In the **`mongo` shell** run the below commands in the following order to:

1. **create the new database** - command `use ironhack-inc`

2. check what is the name of the current database - command `db` .

3. list all of the collections of the current database - command `show collections`.

   &

4. **create a new collection** in that database - command `db.createCollection("employees")`

```bash
use ironhack-inc

db

show collections

db.createCollection("employees");
```

<br>

### Insert new documents to the collection

**Task 2 :**

On your system, using the terminal navigate to the directory of the cloned repository containing the file `employees.json`.

Run the following command **in the terminal** (_not in mongo shell_) in order to import the documents from `employees.json` file in to the newly created database `ironhack-inc` :

```bash
mongoimport --db=ironhack-inc --collection=employees --file=employees.json --jsonArray
```

<br>

### Query the database

Once you have introduced the above documents in the collection `employees` using the your `mongo` shell, perform the following queries:

<br>

- **Task 3**: List all `employees`. You may want to check the methods [`.find()`](https://docs.mongodb.com/manual/reference/method/db.collection.find/#db-collection-find) and [`.pretty()`](https://docs.mongodb.com/manual/reference/method/cursor.pretty/#cursor.pretty)

<br>

- **Task 4:** Find all employees whose `name` is `'Steve'`.

<br>

- **Task 5:** Find all employees whose `age` is greater than `40`.

<br>

- **Task 6:** Find the employee whose extension, `ext` field is `"2143"`.

  If you are not sure how to query the nested `ext` field take a look at the docs here : [Query on Nested Field](https://docs.mongodb.com/manual/tutorial/query-embedded-documents/#query-on-nested-field)

<br>

- **Bonus:** Find and update the employee whose `name` is `"Bob"` and change his `privileges` to `"user"`. You may want to take a look at the method [ `updateOne`](https://kb.objectrocket.com/mongo-db/mongodb-updateone-431).

<hr>
<br>
