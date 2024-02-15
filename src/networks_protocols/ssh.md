# 🔒 SSH

SSH (**S**ecure **S**hell): A protocol for secure network administration and data communication, offering a secure channel over an unsecured network in a client-server architecture.

## History

SSH was first developed by Tatu Ylönen in 1995 as a secure alternative to the unencrypted protocols used for remote administration, such as Telnet and FTP.

It was designed to provide secure communication over an insecure network, using strong encryption to protect the data exchange between the client and the server.

## Structure

SSH uses a combination of asymmetric and symmetric encryption to secure the data exchange between the client and the server.

### Asymmetric Encryption

Asymmetric encryption uses a pair of keys to encrypt and decrypt the data: a public key and a private key.

- **Public Key**: This key is used to encrypt the data and can be freely distributed.
- **Private Key**: This key is used to decrypt the data and must be kept secret.
- **Key Exchange**: The public key is exchanged between the client and the server, and the private key is kept secret by the server.
- **Digital Signature**: The private key is used to create a digital signature, which can be verified using the public key.
- **Certificate**: The public key is often distributed in a digital certificate, which is signed by a trusted third party known as a Certificate Authority (CA).
