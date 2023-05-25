# SSH_KEY_PRIVATE

# Step 1: Generating SSH Keys

### The <span style="color: red;"> ssh-keygen</span> command to generate a new SSH key pair. By default, this will create an RSA key with a size of  <span style="color: blue; font-weight: bold;"> 2048 bits</span>
.

```sh
    ssh-keygen
```

### You can choose a custom location and filename for your keys or press Enter to use the defaults and also specify a passphrase to further secure your key, but this is optional.


This will generate an <span style="background-color: yellow;"> SSH key pair</span>: a public key `id_rsa.pub` and a private key ` id_rsa` . The public key will be used on the remote server, while the private key should be kept securely on your local machine.



# Step 2: Configuring the public key on the remote server
 
- ###  1. Copy of your public key
```sh
cat ~/.ssh/id_rsa.pub
```

- ###  2. Connect to `the remote server` using your usual credentials:

```sh
ssh user@server_address
```
- ###  3. Create the <span style="color: red;"> ~/.ssh directory</span>  on the remote server if it does not already exist: 

``` sh
mkdir -p ~/.ssh
````
- ###  4. Edit the <span style="color: red;"> ~/.ssh/authorized_keys</span>  file on the remote server (or create it if it doesn't exist):

```sh
nano ~/.ssh/authorized_keys

```
- ### 5. Paste the contents of your <span style="color: red;">public key</span>  into this file and save it.

<span style="background-color: yellow;">  Your public key is now configured on the remote server, which will allow you to connect without having to provide a password.</span>

# Step 3: Using SSH keys when connecting to the remote server

  To connect to the remote server using your SSH keys, use the ssh command followed by the user and server address:

````sh
ssh user@server_address

````
 
###  <span style="color: red;"> Note that</span>:
<spanspan style="background-color: yellow;"> Be sure to take appropriate steps to protect your private keys, as they provide access to your servers.</span>
