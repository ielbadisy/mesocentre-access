# Connecting to the server via SSH (Mésocentre configuration)

## Step 1: Generate public and private keys

To establish a secure SSH connection, you'll first need to generate a public and private key pair.

### From Linux:

1. Open your terminal.

2. Type the following command:

```
ssh-keygen -t rsa -b 4096 -o -a 128
```

3. Follow the prompts to enter a new password.

### From Windows:

1. Ensure OpenSSH is installed. If not, install it.

2. Open CMD or PowerShell.

3. Type the same command as above:

```
ssh-keygen -t rsa -b 4096 -o -a 128
```

4. Follow the prompts to enter a new password.

For detailed instructions, refer to [this guide](https://mesocentre.univ-amu.fr/ssh/#deux).

## Step 2: Upload the generated public key

1. Log in to your Copernicus account: [Copernicus User Login](https://mesocentre.univ-amu.fr/copernicus/user.html).

2. Upload the public key file, which can be identified by its `.pub` suffix.

## Step 3: Connect to the server

Use the following command to connect to the server:

```
ssh -i [your_private_key] -p 8822 [username@login.mesocentre.univ-amu.fr]
```

You will be prompted to enter the password you set in Step 1.

## Subsequent connections

After the initial setup, you can connect to the server more simply with these commands:

```
ssh -i [your_private_key] -p 8822 [username@login.mesocentre.univ-amu.fr]
[your_password]
```

Ensure that the `[your_private_key]` file remains in your working directory to maintain the connection.

---

### Notes:

- This configuration needs to be done only once.

- Ensure your private key file is securely stored and not shared.
