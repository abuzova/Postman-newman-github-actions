# Postman + newman + github actions
## Commands Overview
 - Run *npm i to install node.js* dependencies.
 - Run *npm run tern-on-api* to run testing server locally on 3000 port.
 - Run *npm install -g newman* to install newman.
 - Run *npm install -g newman-reporter-htmlextra* to install newman reporter. 
 - Run *npm run test* to run newman runner with petstore.collection.json through API on local server and to run generate the html report.
    
  

## REST API Overview
Routes /products, /orders and /users. Below is a table of supported operations with products as example resource. The same operations are also supports for orders/ and users/.

 | VERB   |	Route         | Input |	Output         |
 | -----  |---------------|-------|----------------|
 | GET    |	/products	  | None  |	Array          |
 | GET    |	/products/:id |	e.g 3 | Object         |
 | POST   |	/products     |	object|	Created object |
 | PUT    |	/products     |	object|	Updated object |
 | DELETE |	/products/:id |	e.g 3 |	Deleted object |

Test examples overview:

 - Test pagination, by way like http://localhost:3000/users?page=1&pageSize=2.
 - Test sorting, by way like http://localhost:3000/users?sortOrder=ASC&sortKey=firstName. You can sort an any resource response using query parameters sortOrder and sortKey.
 - Test status code for REST API (200,400 and so on).
 - Test response time.
 - Test response thanks to json schema validation.