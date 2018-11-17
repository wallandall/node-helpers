# Helpers

Helpers is a list of helpers written to be used in Node applications to simpliy certain tasks

## auth
auth is a list of Functions that can be used to simplify authentication with Passport
- ensureAuthenticated: This helper ensures that a user is authentigated
  - eg:
```
        router.get('/add', ensureAuthenticated, (req, res) => {
           res.render('task/add');
        });
```


## hbs
hbs is a list of helpers that can be used to simplify a number of functions within Handlebar View Templates.

**Dependencies**
- moment


- **truncate**: Truncate is a function that truncates text to a defined length.Truncate takes two parameters: `truncate <Text to truncate> <Number of characters>`.
  - eg: `<p >{{truncate body 150)}</p>`
- **stripTags**: Strip tags is a function that removes html tags from Handlebar templates ie: `<h1>Test</h1>` will be replaced with Plain text. This function takes on one parameter: `stripTags <Text to strip>`
  - eg: `<p >{{stripTags body)}</p>`
- **formatDate**: formatDate is a function that allows you to format dates in Handlebar templates. This function takes on one parameter: `formatDate <Date variable> <Date Format>`
  - eg:
```
       <span class="card-title">
         {{formatDate task.date 'MMMM Do YYYY'}}
       </span>
```
