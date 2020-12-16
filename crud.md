# CRUD

Create, Read, Update, and Delete are four basic types of model functionalities when working with databases.

CRUD identifies all the major functions that are inherent to **relational databases**:
-most commonly implemented type of DB
-consists of data tabled in rows and columns
-connected to other tabes with complementary information by a system of keywords
-includes primary keys and foreign keys

Note: below methods are for Express

# Create

- Allows users to create a new record in the DB.
- Can create a new row and populate it with data that corresponds to each attribute

```sh
app.post('/', (req, res) => {
    // think .map() to find data and manipulate
    // create new item and push onto array of objects
    })
```

# Read/Retrieve

- Allows users to search and retrieve specific records in DB
- Users may be able to find desired records using keywords, or by filtering data based on customized criteria

```sh
app.get('/', (req, res) => {
    // fn to find data
    })
```

# Update

- Used to modify existing records in DB.
- find object and replace

```sh
app.put ('/:id', (req, res) => {
    // find items and check if item is found
    // find index of found object from array of data
    // replace object from data list with updated object
    // think .find() })
```

# Delete

- Remove records from a DB that is no longer needed.

```sh
app.get('/id:', (req, res) => {
    // find item, check if it is found
    // think .splice() method to dete item from data array using index
    })
```
