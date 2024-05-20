explenation for get product function


in the get customer id endpoint, we filter the customer by id, we get the first result and convert it to scalers which is python friendly. we throw a 404 at if the id is not found. we then use the customer schema blueprint to return it in the jsonified format, we can now we can use http://localhost:5000/customers/1   also to get the customer id, we use the filter which is a built in sqlalchemy method.




explenation for the update product function

take an id as the parameter, the parameter will be the id that i enter in postman. we then use the same scaler method to make it python readable, we give an error when the data returned does not match the schema, and if it does match we simply get the price and name of the product



explenation for the delete product

Take an ID as the parameter, the parameter will be the ID that I enter in Postman. Create a delete query to find the product with the given ID and attempt to delete it.

if the product is not found return an error message.
if the product is found, commit the deletion to the database,



explenation for list products


Create a query to select all products from the database.
execute the query and convert the results into a list of scalar objectsPythonfriendly
convert to json with product schema
Return the jsonified list of products.




explenation for add order function, 


to add an order the function first receives customer and product information. It then validates the data to make sure it matches the order schema. Next, a new order is made, and the selected products are correlated with it. The function commits these changes, tells the user it was succsefull


explenation for get order function

this function queries the orders table to find the order with the specified id. It gets the order object from the database and checks if the order exists. If the order is not found, it returns an error message with a status code of 404. then, it formats the order data according to the order schema. returns as json.