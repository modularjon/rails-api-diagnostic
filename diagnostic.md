# Rails API Diagnostic

Place your responses inside the fenced code-blocks where indicated by comments.


What is the purpose of a backend?

```bash
A backend provides acccess to information in a database for a client. It is responsible for interpreting requests, finding and possibly changing the
appropriate data, and then returning the results to the user.
```

Which layer in the MVC pattern is used by the controller to fetch data?

```bash
The model
```

Which layer in the MVC pattern communicates with the model?

```bash
The controller
```

Why don't we use views in our interpretation of the MVC pattern?

```bash
Views are not necessary serverside in an SPA. The client handles the view.
```

What does C.R.U.D stand for?

```bash
Create, Read, Update, Delete
```

In which part of the MVC pattern can we find C.R.U.D actions?

```bash
The actions take place in the model, when it accesses the appropriate database.
```
List at least 5 standard actions that C.R.U.D corresponds to?

```bash
index, show, create, update, destroy
```

A user action fires a `GET` request for `person/1`. Explain in detail each step
required for data to be returned to the client. (bullet points or ordered list)

```bash
1. Web server receives the http and determines which controller to access based
on the request syntax (get 'person/1', to: 'people#show').

2. Controller executes the method required (show), which then accesses the appropriate model.

3. The model accesses the SELECTS id = 1 FROM the database and sends it back to the constroller.

4. The controller sends the data (repackaged as json, text, etc.) to the web server.

5. The web server sends the data to the client.

6. The client renders the data in html or whatever.
```

What is the command to generate a new rails-api app?

```bash
rails-api new app_name -T --database=postgresql
```

What is the command to start an instance of a rails server?

```bash
rails s
```

What are the commands to drop, create and migrate a database? (3 bullet points)

```bash
• rake db:drop
• rake db:create
• rake db:migrate
```

What is the command to scaffold a pet with a name and an age?

```bash
rails g scaffold post name:string age:integer
```

List two advantages of using serializers? (2 bullet points)

```bash
• Keeps code modular and semantic
• Makes app less fragile
```
