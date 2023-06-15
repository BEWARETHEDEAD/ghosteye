GHOST EYE:

**this is an accurate system for identifying a user's wallet, using the data of his Telegram account (at the moment, only @username)**

**The value itself is a centralized database, which is replenished automatically with the help of: bots for NFT holders, parsing of GetGems collections, detection of Telegram @username associated with the GetGems profile**


**· [UPDATES](https://github.com/BEWARETHEDEAD/ghosteye/blob/main/upds.md) ·**


# GHOST EYE Quick Start

- Get User Info
``` Python 

import requests

headers = {
  'Content-Type': 'application/json'
}

data = {
  'username': 'username',
  #'user_id': 1234567890  ( Optional )
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

headers = {
  'Content-Type': 'application/json'
}

data = {
  'user_id': 1234567890,
  'username': 'username',
  'name': 'Name',
  'wallet': 'EQAsl59qOy9C2XL5452lGbHU9bI3l4lhRaopeNZ82NRK8nlA'
}

r = requests.get(f'https://d7d0-195-2-75-73.eu.ngrok.io/ghosteye/add_user', headers=headers, json=data)

print(r.json()) #Add full info of user
```

Example request answer:

``` 
{"user": "succesfully added!"}
```
