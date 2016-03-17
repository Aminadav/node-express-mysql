Thank for trying out this NPM module. The status of the project is stable. You can use it for you own project.
If you have any suggestion and idea, you welcome to push request. I'm going to continue improve it.
Any pull-request is welcome. Even changes to the screenshots and improve the English.

# This library let you many things:

- Let you download data from mysql as JSON or CSV. It support millions of records using stream. Your express server will never hold all the data in memory. IT stream from the DB server directly to your client.
- Let your run any kind of query. (Not just specific table)
- It gives your interface to see the data in the database, and add filter and orders.

## How to install it 

	npm i -s node-express-mysql

	var em=require('express-mysql')
	app.use('/ourdb',em({
		"host":"db.example.io",
		"database":"example",
		"user":"user",
		"password":"password"
	}))

To see the databse go to:

	yourapp.com/ourdb/frontend

You can set it to any other subdirectory you want. Not just `/ourdb`


## Queries example to the backend:

	/ourdb/rows/?table=table_name&format=csv

To download specific query as json:

	/ourdb/rows/?query=select * from moshe&format=csv

To limit to first 100 rows
	
	/ourdb/rows/?query=select * from moshe&format=csv&limit=100

## Frontend interface	

	Using the interface you can see the database, and download data.
	You can save the URL of the downloaded data, so each time you use the same URL, refreshed data will be downloaded.


## Contributions.

	We need your help, to make it look nicer. 

## Roadmap
	
	Support for JSONP 

## Screenshot

![](http://snag.gy/CfBGS.jpg)