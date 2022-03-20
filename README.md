# Project Summary <br>
<p>In this workshop you will create a CRUD API that Creates, Reads, Updates and Deletes items from a DynamoDB table. The API will run serverless, so there is no management of the underlying infrastructure and scaling is done automatically.</p>

![Architectural Diagram!](/assets/images/san-juan-mountains.jpg "Architectural Diagram!")



## INVOKE_URL=https://6xnkmpnrad.execute-api.us-east-1.amazonaws.com/

**Sample Code to create an item**<br>
`curl -X "PUT" -H "Content-Type: application/json" -d "{
    \"id\": \"abcdef234\",
    \"price\": 12345,
    \"name\": \"myitem\"
}" $INVOKE_URL/items`



### Use the following command to list all items.

**To get all items:**<br>
Use the following command to list all items.<br>
`curl -s $INVOKE_URL/items | js-beautify` <br>


**To get an item:**<br>
Use the following command to get an item by its ID.<br>
`curl -s $INVOKE_URL/items/abcdef234 | js-beautify`<br>

**To delete an item:**<br>
Use the following command to delete an item.<br>
`curl -X "DELETE" $INVOKE_URL/items/abcdef234`<br>
