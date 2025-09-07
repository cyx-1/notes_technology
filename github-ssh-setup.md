# GitHub

## GitHub SSH Setup
- using ssh key to work with GitHub is easy
  - for example, the following command should clone the repository
  ```
  git clone git@github.com:cyx-1/home.git
  ```
- if you have a public / private key pair, upload the public key via GitHub.com website
  - github/settings/"SSH and PGP keys"/new ssh keys
- if you don't have the keys, use the following command to generate:
```
ssh-keygen -t ed25519 -C "user@emailservice.com"
  - this would generate the key at home/.ssh/id_ed25519.pub
  - choose default for both questions by pressing enter
    - file to save as
    - empty passphrase
```
- for more information, see: https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh

Back to [index](index.md)