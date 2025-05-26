# End-to-End-Encrypted-Chat-App
# 🔐 End-to-End Encrypted Chat App (Terminal-Based)

This is a simple terminal-based chat application with **end-to-end encryption** using **RSA** for key exchange and **AES** for message encryption.

## 🚀 Features
- RSA key pair generation (2048-bit)
- AES session key encrypted with recipient's RSA public key
- Secure encrypted messaging over TCP sockets
- Simple, secure, and easy to understand code structure

## 📁 Project Structure
```
encrypted-chat-app/
├── client/
│   └── client.py
├── server/
│   └── server.py
├── crypto/
│   └── rsa_utils.py
├── README.md
└── requirements.txt
```

## ⚙️ Installation
1. Clone this repo or download the ZIP.
2. Install dependencies:
```bash
pip install pycryptodome
```

## 🧪 How to Use
### Step 1: Start the Server
```bash
python server/server.py
```
Copy the public key printed in the terminal.

### Step 2: Configure the Client
Open `client/client.py` and paste the copied public key in:
```python
SERVER_PUBLIC_KEY = b"""-----BEGIN PUBLIC KEY-----
...paste here...
-----END PUBLIC KEY-----"""
```

### Step 3: Run the Client
```bash
python client/client.py
```

Type messages to send securely. Type `exit` to disconnect.

---

## 🔐 Encryption Details
- **RSA (2048-bit)** for exchanging AES key
- **AES (128-bit, EAX mode)** for encrypting/decrypting messages

## 📚 Dependencies
- Python 3.6+
- `pycryptodome` library

## 📄 License
MIT License

---

Made with 💻 by Mahesh Negi — a project for demonstrating real-world cryptographic principles in action.
