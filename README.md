# auth_service
This microservice handles user authentication, including registering new users and logging in with existing credentials.

You can make HTTP requests to the /register and /login endpoints using any HTTP client. 

register request example:
import requests

url = 'http://localhost:5000/register'
data = {'username': 'yourusername', 'password': 'yourpassword'}
response = requests.post(url, json=data)

print(response.status_code)
print(response.json())

login request example:
import requests

url = 'http://localhost:5000/login'
data = {'username': 'yourusername', 'password': 'yourpassword'}
response = requests.post(url, json=data)

print(response.status_code)
print(response.json())

The microservice returns a JSON response with a status code. 
- 400: error
- 401: unauthorized
- 409: conflict
- 200: ok
- 201: registration success

Install dependencies using pip:
pip install flask flask-bcrypt portalocker

Run using:
python auth_service.py
