# 🔒 SSL/TLS

SSL/TLS (**S**ecure **S**ockets **L**ayer/**T**ransport **L**ayer **S**ecurity): Protocols that provide communications security over a computer network.
They are most famously used for securing connections between web browsers and servers, including the encryption of our internet transactions.

## History

SSL was first developed by Netscape Communications in 1994 to secure the communication between web browsers and servers.

TLS is the successor to SSL, and it was first defined in 1999 by the Internet Engineering Task Force (IETF) as an open standard protocol.

## Structure

SSL/TLS protocols use a combination of asymmetric and symmetric encryption to secure the data exchange between the client and the server.

### Asymmetric Encryption

Asymmetric encryption uses a pair of keys to encrypt and decrypt the data: a public key and a private key.

- **Public Key**: This key is used to encrypt the data and can be freely distributed.
- **Private Key**: This key is used to decrypt the data and must be kept secret.
- **Key Exchange**: The public key is exchanged between the client and the server, and the private key is kept secret by the server.
- **Digital Signature**: The private key is used to create a digital signature, which can be verified using the public key.
- **Certificate**: The public key is often distributed in a digital certificate, which is signed by a trusted third party known as a Certificate Authority (CA).
