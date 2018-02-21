# get-firebase-id-token
Python script for getting [Firebase ID and refresh tokens](https://firebase.google.com/docs/auth/users#auth_tokens) 
from a user 
ID (UID). Useful for testing & debugging. 

ID tokens last for 1 hour (set by Firebase).

## Setup

1. Install [firebase_admin](https://firebase.google.com/docs/admin/setup#add_the_sdk): `
$ pip install --user python_firebase`
2. Fill out the configuration constants in get_firebase_id_token.py

## Usage
As an import (returns a dict):
```python
import get_firebase_id_token

uid = "Firebase user id"
print get_firebase_id_token.get_token(uid)

```

Command line (prints only the ID token):
```commandline
$ python get_firebase_id_token.py <UID>
```