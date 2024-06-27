1. **Method**: The sort of action we want the server to take
	1. Get: Retrieve information, don't cause any server changes
	2. Post: Create new objects on the server
	3. Delete: Ask the server to destroy 
2. **Route**: A description of the server resource we want to retrieve, create or change
3. **Headers**: Metadata for our request, for example information to the server about the format of the message body.
4. **Body**: Arbitrary text that can be sent to the server to help it full fill our request.

HTTP responses:
- **Status Code and Message** : What happened, when the server server handled the request
	- 200: OK
	- 404: Not Found
	- 500: Internal Server Error
	- 501: Not Implemented
- **Headers**: Metadata from the server, for example: the time data was generated
- **Body**: Arbitrary text back to the client


