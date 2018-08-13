# Check the Fingerprint of a Public Key

Recently a server that I SSH to was migrated to a new hosting provider and the fingerprint of the public key changed.

You can verify the fingerprint of a key by running: `ssh-keygen -lf <path/to/key.pub>`

On your local machine the key will probably be at `~/.ssh/id_rsa.pub`, on your server it'll probably be at `/etc/ssh/ssh_host_rsa_key.pub`
