Fast API is a modern high performance web framework for building APIs with python .

Built on :
Starlette - It manages how your api receives requests and sends back response 

Pydantic - Does data validation in fast api , checks weather the data coming is in the correct format .

Why FAST API ?
- This works very fast to run and would be very less latency .
- Very fast to code and removes unnecessary code .

SGI : Server Gateway Interface
 It converts the http request to python code which the api can understand , so it basically is a converter between the web server and the api code ![[Screenshot 2025-09-28 at 6.08.44 PM.png]]

SGI types :
- WSGI and ASGI .
- WSGI is synchronous in nature that is it can process one request at a time and has blocking nature that is it blocks other requests while fulfilling other request . Used in flask .
- To implement WSGI we use werkzeung library .
- Gunicorn is a flask web server and has the same issue as WSGI ( synchronous and blocking ) .

- ASGI is a asynchronous SGI . Used in FastAPI .
- ASGI is implemented using starlettle and the web server is unicorn .
- FastApi can implement async and await feature of python . This helps in parallel processing .
- This means it can process concurrent requests . 
- Due to this FastAPI is fast .

# Why is it faster to code ?
1. Automatic input validation (data type check using pydantic ) .
2. Auto generated interactive documentation (automatically documents the web applications endpoints used for apis of that web application )
3. Seamless integration with modern ecosystem (ML / DL library , OAuth , SQL ) .
