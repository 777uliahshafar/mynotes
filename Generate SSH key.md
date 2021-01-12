# Generating SSH key on Mac

- Run command `ssh-keygen -b 2048 -t rsa`.
- Set a passphrase for protect the key,it is optional. This will create a hidden directory ~/.ssh and two key for public and private.
- Grants administrator access to public key with `chmod 600 .ssh/id_rsa.pub`.
- Add private key to keychain Mac by `ssh-add -K ~/.ssh/id_rsa`. It is important to keep private key only on our computer.
- Preview key using cat for instance: `cat .ssh/id_rsa.pub`.
- Avoid using passphrase everytime using key by edit config with nano and add this following text:  `nano .ssh/config`
```
Host *
    UseKeychain yes
```
