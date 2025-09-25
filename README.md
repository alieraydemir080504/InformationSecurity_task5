# InformationSecurity_task5

## x) Read and summarize

### Schneier 2015: Applied Cryptography

- Cryptography is the science of protecting information so only the intended person can read it
- A normal message is called plaintext, and when it is hidden it becomes ciphertext
- The process of changing plaintext into ciphertext is encryption, the reverse process, making ciphertext readable again, is decryption
- People who create and study methods for encryption are cryptographers, those who try to break these methods are cryptanalyst
- These ideas are not only for text, they can be used for images, audio, video, or any kind of data

### Karvinen 2023

- Both people generate a keypair (public + private)
- Public key is shared, private key is secret
- Each person must verify the others public key by checking the fingerprint
- Sender encrypts the message with recipient’s public key
- Sender can also sign with their own private key
- Receiver decrypts with their private key and verifies the signature
