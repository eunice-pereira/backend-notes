# CRUD

Create, Read, Update, and Delete are four basic types of model functionalities when working with databases.

CRUD identifies all the major functions that are inherent to **relational databases**:

-most commonly implemented type of DB
-consists of data tabled in rows and columns
-connected to other tabes with complementary information by a system of keywords
-includes primary keys and foreign keys

Note: below methods are for Express

# Create

- Allows users to create a new record in the DB (like sign up)
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
- i.e. login

`User.findAll()`
-returns an Array
`User.findOne()` - returns an Object (or null)
`User.findByPk()` - find user by primary key

# Update

- Used to modify existing records in DB (ex. edit profile pic)
- Updates are completed in two parts:
  - retrieve item in database by primary key
  - edit item, now showing in HTML, and post new edit
  - this will not change item's id; will only update contents in DB

```sh
app.get('/:id', (req, res) => {
    User.update({where: id})
})
```

# Delete

- Remove records from a DB that is no longer needed.

```sh
app.get('/id:', (req, res) => {
    // find item by id
    User.destroy({where: id})
    })
```
