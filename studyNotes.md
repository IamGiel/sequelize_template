# ** A full stack app folder organization.

###   `server.js` - 
  
  contains the connection set-up.  Inisde usually we have the dependencies.
we will see:

```
--dependencies
var express = require ('express');
var bodyParser = require('body-parser');
```
```
<!-- set up the express app -->
var app = express();
var PORT = process.env.PORT || 8080;
```
```
<!--  express app bodyParser -->
<!-- see documentation usually and data acquired in `req.body` -->
app.use(bodyParser.json); 
```
```
<!-- static directory -->
<!-- this is for the css/html templates -->
app.use(express.static(pathTo/fileName))
```
```
<!-- routing -->
require('path/To/API_ROUTE.js')(app);
require('path/To/HTML_ROUTE.js')(app);
```

```
<!-- port listening to... -->
app.listen(function(){
	console.log("listening on PORT: " + 8080)
})
```

*****************************
###   `app.js` - 

`There are four folders inside app.js: Ill use mnemonics to remember the folders`

mnemonic = `PURO COMO` = as pure... (in Spanish)

PURO COMO:

ACRONYMS  | STANDS FOR
------------- | -------------
PU  | public
RO | router
CO  | config
MO | model

### Public
1. [x] index.html
	* [x] main templates
	
2. [x] layout folder
       * [x]main.handlebars
       
3. [x] js folder
       * [x]index.js
       * [x]logic to the applciation using javascirpt or jquery

3. [x] css folder
       * [x]index.css
       * [x]style the pages
       

       

`public`
--views/layouts
	--index.html `OR`
	--layouts
		--main.handlebars

`routes`
--API_routes.js
	-- may contains MySQL codes for CRUD
	-- may contain SEQUELIZE codes for CRUD
	-- may contain HTTP Requests for CRUD
--HTML_routes.js
	--contains the root routes of each html files

	

*****************************











