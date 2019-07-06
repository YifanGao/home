# Passwordless SSH login

Reference [here](https://www.tecmint.com/ssh-passwordless-login-using-ssh-keygen-in-5-easy-steps/)

Generate an ECDSA key pair,

~~~~
ssh-keygen  -b 521 -t ecdsa -f $(KEY_NAME)
~~~~

or generate an RSA key pair,

~~~~
ssh-keygen  -b 8192 -t rsa -f $(KEY_NAME)
~~~~

When prompted up 'enter passphrase', simply press enter twice so that passphrase is empty.

It'll generate two textual files: $(KEY_NAME) and $(KEY_NAME).pub . The former is your private key that you might want to keep well, and the latter is the public key you gave to everybody.