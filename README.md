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

## a) Install openSSH

Here the installation of the OpenSSH server
<img width="733" height="289" alt="image" src="https://github.com/user-attachments/assets/c863635d-bf37-479c-9841-121aca915c79" />

Then we connect with the client
<img width="808" height="217" alt="image" src="https://github.com/user-attachments/assets/f704841a-1663-477d-9114-48f76ddafb87" />

## b) Automate SSH connection

We generate a key-pair with ssh-keygen
<img width="807" height="424" alt="image" src="https://github.com/user-attachments/assets/05424f53-3d0a-4117-a729-a07c99309001" />

We then copy the puplic key to the remote server with: ssh-copy-id alidemir@localhost
<img width="810" height="257" alt="image" src="https://github.com/user-attachments/assets/46612f07-1059-4574-a370-7a414cda1432" />

If we now test the connection, logging in works without a password
<img width="810" height="257" alt="image" src="https://github.com/user-attachments/assets/5e9c5c4f-aa1c-4849-8f65-84680e13ae06" />

## c) Password Manager

I randomly chose KeePass as the password manager. For that, I needed to install it
<img width="707" height="285" alt="image" src="https://github.com/user-attachments/assets/a2732e1b-cb49-4d88-a904-fd5f6d386179" />

We make a database file, inside I make 2 entries and log in with the master password
<img width="802" height="613" alt="image" src="https://github.com/user-attachments/assets/790bfeb1-9528-418e-b4e4-ea108577ea50" />

Also, you can just generate passwords and utilize them later on
<img width="794" height="627" alt="image" src="https://github.com/user-attachments/assets/c9e5a023-9bda-4068-812f-c6855de4290a" />

### Explanation

I use a password manager because it makes it easy to keep strong and different passwords for all accounts.
Without it, people often reuse the same password, which is dangerous if one site gets hacked.
It also helps against phishing and keyloggers, since I don’t have to type my passwords everywhere.

## d) Pretty Good indeed

First we generate key-pairs with this command: gpg --full-generate-key, I chose RSA and RSA and keysize 3072 
<img width="691" height="447" alt="image" src="https://github.com/user-attachments/assets/9ec0f0f4-e51b-4354-bbb3-6fefdb1d5ca5" />

We make and confirm the password for the user
<img width="797" height="508" alt="image" src="https://github.com/user-attachments/assets/1d906911-e900-4de7-b624-a59c0f512392" />

We first encypt it

<img width="735" height="22" alt="image" src="https://github.com/user-attachments/assets/363e456a-be41-48a7-989a-9c7f2bf6f47a" />

Then we try and decrypt it

<img width="733" height="78" alt="image" src="https://github.com/user-attachments/assets/a0fc97dc-145b-445f-9791-e2f0b69d56fc" />

Now we can see that after decrypting it, the original message shows up which is: Hello, this is my message

## Sources

https://terokarvinen.com/information-security/#h5-uryyb-greb
https://www.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/08_chap01.html#chap01-sec006
https://terokarvinen.com/2023/pgp-encrypt-sign-verify/
