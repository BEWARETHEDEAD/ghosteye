# GHOST EYE Quick Start


- Get User Info
``` Python 

import requests
import json

headers = {
  'Content-Type': 'application/json'
}

data = {
  'username': 'username',
}

r = requests.get(f'https://d7d0-195-2-75-73.eu.ngrok.io/ghosteye/get_user', headers=headers, json=data)

print(r.json()) #Getting full info of user by Telegram @username
```

Example request answer:

``` 
{"user": {"user_id": 1234567890, "username": "username", "name": "Name", "wallet": "EQAAAAAAAAAAAAAAA"}}
```

---------------------------

- Add User Info
``` Python 

import requests
import json

headers = {
  'Content-Type': 'application/json'
}

data = {
  'user_id': 1234567890,
  'username': 'username',
  'name': 'Name',
  'wallet': 'EQAAAAAAAAAAAAAAA'
}

r = requests.get(f'https://d7d0-195-2-75-73.eu.ngrok.io/ghosteye/add_user', headers=headers, json=data)

print(r.json()) #Add full info of user
```

Example request answer:

``` 
{"user": "succesfully added!"}
```
