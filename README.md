# Back-End
Back end server created using node js, express, and knex.

Register:

POST -address-/auth/register
Takes in a User object
    {
        Username: -name-,
        Password: -password-,
        Email: -email-,
        Account: -(Editor or Subsciber)-
    }

Returns an object with Username and Account
    {
        Username: -name-,
        Account: -account-
    }


Login:

POST -address-/auth/login

Takes in an object
    {
        Username: -name-,
        Password: -password-
    }
Returns and object with user id and a token
    {
        id: -id-,
        token: -token-
    }

Get all entries:

GET -address-/api/entries
returns an array of entry objects with data fields:

id, Author, Title, Created, Category, AverageRating 


Get a single entry by id

GET -address-/api/entries/:id
returns an object with data fields:

id, Author, Title, Created, Category, AverageRating 

Get an entries content blocks

Get -address-/api/entries/:id/content
returns an array of objects for each content block with fields:

Step,Heading,Content


