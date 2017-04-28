# Rails API Diagnostic

Place your responses inside the fenced code-blocks where indicated by comments.

What is the purpose of a backend?

```md
The backend does the heavy lifting.  It stores data, routes client requests and basically
supports an application.
```

Which layer in the MVC pattern is used by the controller to fetch data?

```md
The Model, which talks to the database, crunches numbers and retrieves whatever the client needs from the database
```

Which layer in the MVC pattern communicates with the model?

```md
The Controller (it works with both the Model and the View)
```

Why don't we use views in our interpretation of the MVC pattern?

```md
Because the view is what the user sees and interacts with (visual representation of the data they requested), so if we used them in our interpretation, I guess it would have just been someone standing there being poked or typed on?
```

What does C.R.U.D stand for?

```md
Create
Read
Update
Delete
```

In which part of the MVC pattern can we find C.R.U.D actions?

```md
In the Controller.  The Controller will send a request to
either create something, GET something, PATCH something or DELETE something (depending on the request)
```

List at least 5 standard rails actions that C.R.U.D requests correspond to?

```md
index, create, show, update, destory
```

A user action fires a `GET` request for `/people/1`. Explain in detail each step
required for data to be returned to the client. (bullet points or ordered list)

```md
  - Client request is sent to server
  - Server interacts with Controller to find the People Controller
  - People Controller then requests the data from the People Model
  - If the data exists, the People Model will return it to the People Controller > Controller > Server > Client.  If the data does not exist, it will return a 400 error (404 not found)
```

What is the command to generate a new rails-api app?

```bash
rails generate
```

What is the command to start an instance of a rails server?

```bash
bin/rails server
```

What are the commands to drop, create, migrate and seed a database from the command
line? (5 bullet points)

```bash
db:drop
db:create
db:migrate
bd:seed
```

What is the command to scaffold a pet with a name and age attributes (hint:
Also think of the data types for each attribute)?

```bash
bin/rails generate model Pet name:string age:integer
```
