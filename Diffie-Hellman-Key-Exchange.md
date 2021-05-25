# Diffie-Hellman-Key-Exchange

![Diffie-Hellman-Key-Exchange](https://user-images.githubusercontent.com/27002592/75615939-372ebb00-5b42-11ea-9b6e-df4689b84f07.png)

- two parties (Alice and Bob)
- don’t know each other
- communicate over insecure channel
- need both the same key to use symmetric cryptography, e.g. AES

Alice starts. She generates a key, puts it in a box, and locks it – with a padlock that only she has the key to open.
She sends the box to Bob.
 
Bob cannot open the box, so he cannot get the key. Now for the trick: He takes his own padlock, double locks the box
and sends it back to Alice.
 
Alice now removes her padlock. Obviously, she cannot remove Bob’s padlock.
She just returns the box to Bob – which is now only closed with Bob’s padlock.

So, Bob can open the box… and has now the key Alice generated.