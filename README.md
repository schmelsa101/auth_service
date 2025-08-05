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

<img width="873" height="429" alt="image" src="https://github.com/user-attachments/assets/5ed9a652-b501-4e83-9486-2f4c501ba18f" />

Communication Ground Rules: 
Our primary mode of communication will be Teams. If needed, we will also use Canvas discussions for assignment-specific discussions. Each team member is expected to respond to messages within 12 hours to maintain workflow efficiency. Most communication will be asynchronous, but if a live discussion is needed, we will coordinate a time that works for all members.
