# Add `users`

### Using Postman

1. **Open Postman** and create a new request.
2. Set the request type to **POST**.
3. Enter the URL for your API endpoint that adds a user, for example:
```shell
https://yourapi.com/api/users
```
4. In the **Body** tab, select **raw** and set the type to **JSON**.
5. Add the JSON payload for the new user. For example:
```shell
{
  "first_name": "John",
  "last_name": "Doe",
  "email": "john.doe@example.com",
  "privacy": "public"
}
```
6. Click on the **Send** button to execute the request.
7. You should see the response indicating that the user has been added.

### Using Curl

You can use the following curl command in your terminal or command prompt to make the same POST request:
```shell
bash
curl -X POST "https://yourapi.com/api/users" \
-H "Content-Type: application/json" \
-d '{
  "first_name": "John",
  "last_name": "Doe",
  "email": "john.doe@example.com",
  "privacy": "public"
}'
```

### Example Response

The expected JSON response after successfully adding the user might look like this:
```js
{
  "id": 5,
  "first_name": "John",
  "last_name": "Doe",
  "email": "john.doe@example.com",
  "privacy": "public"
}
```
### Note:
- Replace `https://yourapi.com/api/users` with the actual endpoint of your API that adds a user.
- Ensure that the email is unique and does not already exist in the database.
- Ensure your API server is running and accessible when you execute these requests.