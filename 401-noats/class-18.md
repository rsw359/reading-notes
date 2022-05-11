# class 18

## There are three key aspects of data encryption:

- Encryption: scrambling the data according to a secret key (in this case, the alphabet shift).
- Decryption: recovering the original data from scrambled data by using the secret key.
- Code cracking: uncovering the original data without knowing the secret, by using a variety of clever techniques.

Whenever we consider a possible encryption technique, we need to think about all those aspects: how easy is it to encrypt? how easy is it to decrypt? And most importantly, how easy is it for a nefarious individual to crack the code?

Taken from Khan Academy

- Julius Caesar used an encryption created by shifting the letters by a specific number of spaces. Then the ‘plaintext’ could be decrypted using a cypher. This type of encryption can be easily broken due to letter frequency.

## Video

[https://www.youtube.com/watch?v=jhXCTbFnK8o](https://www.youtube.com/watch?v=jhXCTbFnK8o)

Cryptography, at its most fundamental level, requires two steps: encryption and decryption. The encryption process uses a cipher in order to encrypt plaintext and turn it into ciphertext. Decryption, on the other hand, applies that same cipher to turn the ciphertext back into plaintext.

There are four primary types of cryptography in use today, each with its own unique advantages and disadvantages.

They are called hashing, symmetric cryptography, asymmetric cryptography, and key exchange algorithms.

***Hashing*** is a type of cryptography that changes a message into an unreadable string of text for the purpose of verifying the message’s contents, *not* hiding the message itself.

***Symmetric Cryptography***, likely the most traditional form of cryptography, is also the system with which you are probably most familiar.

This type of cryptography uses a single key to encrypt a message and then decrypt that message upon delivery.

Since symmetric cryptography requires that you have a secure channel for delivering the crypto key to the recipient, this type of cryptography is all but useless for transmitting data (after all, if you have a secure way to deliver the key, why not deliver the message in the same manner?).

***Asymmetric cryptography*** (as the name suggests) uses two different keys for encryption and decryption, as opposed to the single key used in symmetric cryptography.

The first key is a public key used to encrypt a message, and the second is a private key which is used to decrypt them. The great part about this system is that only the private key can be used to decrypt encrypted messages sent from a public key.

***A key exchange algorithm,*** like Diffie-Hellman, is used to safely exchange encryption keys with an unknown party.

Unlike other forms of encryption, you are not sharing information during the key exchange. The end goal is to create an encryption key with another party that can later be used with the aforementioned forms of cryptography.

Notes taken from: [https://thebestvpn.com/cryptography/#ciphers](https://thebestvpn.com/cryptography/#ciphers)