# AES-Cryptographic-algorithm-implementation- #
This is a Python implementation of the Advanced Encryption Standard (AES) algorithm, a widely-used symmetric encryption algorithm. It uses the Crypto library to provide the implementation of the AES cipher and the hashlib library to compute the SHA-256 hash of the key used for encryption and decryption.

## Usage: ##
To use the AES cipher, import the AESCipher class from the AES module and create an instance of the class with a key:
``` 
from AES import AESCipher

key = 'mysecretkey'
cipher = AESCipher(key)
 ```
The AESCipher class provides two methods: encrypt and decrypt, which can be used to encrypt and decrypt strings, respectively:

```
plaintext = 'This is a secret message'
encrypted = cipher.encrypt(plaintext)
print(encrypted)  # Output: b'MzRkNTY5NjFkMzI5MmRlMmQ3M2E5NjZmM2M5NzE5M2I='

decrypted = cipher.decrypt(encrypted)
print(decrypted)  # Output: 'This is a secret message'

```
The encrypt method returns the encrypted version of the input string as a base64-encoded string, and the decrypt method takes a base64-encoded encrypted string as input and returns the decrypted version of the string.


## Padding ##
The AESCipher class uses the PKCS#7 padding scheme to ensure that the length of the input plaintext is a multiple of the block size (16 bytes) required by the AES algorithm. Padding is added using the __pad method and removed using the __unpad method.


## Requirements: ## 
Python 3.6 or higher
Crypto library:
```pip install pycrypto```

### References ###
Advanced Encryption Standard (AES)
Crypto library documentation
hashlib library documentation
