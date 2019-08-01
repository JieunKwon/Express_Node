# Express and Node JS

> Install Express

    npm install express -g

> Create new app

    express --session --view=ejs --css css app_name
    
    
> View engine setup and use it

- app.js 


    var express = require('express');
    
    ...
    
    var app = express();
    
    ...
    
    // setup views and EJS extension 
    
    app.set('views', path.join(__dirname, 'views'));
    app.set('view engine', 'ejs');
    
    ...
    
- routes/index.js

    var express = require('express');
    var router = express.Router();

    // GET index page with title 
    router.get('/', function(req, res, next) {
      res.render('index', { title: 'Express Index Page Test' });
    });
 
    module.exports = router;

- views/index.ejs

** Express EJS Extend : EJS is a simple templating language that lets you generate HTML markup with plain JavaScript

    <html>
      <head>
        <title><%= title %></title> 
      </head>
      <body>
        <h1><%= title %></h1> 
      </body>
    </html>
    
    
