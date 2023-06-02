# Firebase ID Token Generator - Python
Python script for generating [Firebase ID and refresh tokens](https://firebase.google.com/docs/auth/users#auth_tokens) 
from a user ID (UID). Useful for testing & debugging. 

ID tokens last for 1 hour (set by Firebase).

## Setup

1. Install [firebase_admin](https://firebase.google.com/docs/admin/setup#add_the_sdk) and all necessary packages: `
$ pip install --user -r requiremets.txt`
2. Generate Firebase Private Key
`Firebase Console > Settings > Service Accounts > Generate New Private key`
and store in in current directory and rename it to `key.json`
3. Create .env file in current directory and fill out
`WEB_API_KEY` from `Firebase Console > Settings > General > Web API Key` and `PROJECT_ID`

## Usage
As an import (returns a dict):
```python
import firebase_token_generator

uid = "Firebase user id"
print firebase_token_generator.get_token(uid)

```

Command line (prints only the ID token):
```commandline
$ python firebase_token_generator.py <UID>
```