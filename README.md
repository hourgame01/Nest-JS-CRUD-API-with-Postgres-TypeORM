#ref:
https://github.com/hourgame01/Nest-JS-CRUD-API-with-Postgres-TypeORM

#purpose:
CRUD API sample(server side)

#requirement:
##app server:
Nodejs => https://nodejs.org/en
##database:
Postgresql => https://www.postgresql.org/
##postman:
Postman => https://www.postman.com/

#install:
$ git clone https://github.com/hourgame01/Nest-JS-CRUD-API-with-Postgres-TypeORM.git
$ cd Nest-JS-CRUD-API-with-Postgres-TypeORM
$ npm install

#config:
##db:
$ nano src/app.module.ts
type: 'postgres',
host: '<host>',
port: <port>,
username: '<user>',
password: '<password>',
database: '<database_name>',

#run:
$ npm run start:dev

#test api:
##get products
Get: http://<host>:3002/products/
##get single product
Get: http://<host>:3002/products/getOne
##create new product
Post: http://<host>:3002/products
Body: raw(json)
{
    "title": "title1",
    "category": "category1",
    "subcategory": "subcategory1",
    "description": "description1",
    "status": "status1"
}
##update product
Post: http://<host>:3002/products/update?id=2
Body: raw(json)
{
    "title": "title2",
    "category": "category2",
    "subcategory": "subcategory2",
    "description": "description2",
    "status": "status2"
}
##delete product
Post: http://<host>:3002/products/delete?id=2
Body: raw(json)
{}

