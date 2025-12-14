# my-tenth-repo
repo
import json
from cryptography.fernet import Fernet

key = Fernet.generate_key()
cipher = Fernet(key)

passwords = {"gmail": "mypassword123"}
encrypte = cipher.encrypt(json.dumps(passwords).encode())

with open("passwords.enc", "wb") as f:
    f.write(encrypted)

print("Passwords encrypted and saved!")
