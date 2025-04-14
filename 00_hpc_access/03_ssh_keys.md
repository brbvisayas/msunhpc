# 03 – SSH Keys for Passwordless Access

SSH keys allow you to connect to the HPC cluster **without entering your password every time**, improving both security and convenience.

---

## Step 1: Generate an SSH Key (on your local machine)

If you haven’t already created a key pair, run:
<pre>
<code> ```bash
ssh-keygen -t rsa 
```</code>
<pre>
	•	Press Enter to accept the default file location (~/.ssh/id_rsa)
	•	You can leave the passphrase empty or set one for extra protection

This creates a key pair:
	•	Private key: ~/.ssh/id_rsa (keep this secret)
	•	Public key: ~/.ssh/id_rsa.pub (safe to share)

## Step 2: Copy Your Public Key to the HPC Cluster

```bash 
ssh-copy-id -p 2222 yourusername@35.221.236.185

Enter your password once when prompted.

If ssh-copy-id is unavailable, manually copy the contents of ~/.ssh/id_rsa.pub into the ~/.ssh/authorized_keys file on the remote machine.

## Step 3: Test the Connection
```bash
ssh -p 2222 yourusername@35.221.236.185
