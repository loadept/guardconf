# Guardconf
This script allows you to configure and add
new peers in the Wireguard configuration file,
as well as generate public and private keys
for these peers.

# Instalation
First download the file

**curl**
```bash
curl https://raw.githubusercontent.com/loadept/guardconf/refs/heads/master/bin/guardconf -o guardconf
```
**wget**
``` bash
wget https://raw.githubusercontent.com/loadept/guardconf/refs/heads/master/bin/guardconf
```

Then we assign execution permissions
```bash
chmod 744 guardconf
```

Now we are going to move the script to the **PATH**, so we can run it from anywhere.
We can move this script to the **/usr/bin** directory, but for convenience we will
use the **~/.local/bin** directory, so that we can have the script available only
for our user.

We create the folder **~/.local/bin** if it does not exist.
```bash
mkdir ~/.local/bin
```

Now we move the file
```bash
mv ./guardconf ~/.local/bin
```

With this it should be done, but first we must make sure that **~/.local/bin** is in the **PATH**.
```bash
echo $PATH
```
If we go something like `:/home/user/.local/bin` it means that it is available in the **PATH**.

If it is not available we will export it by adding this line in `.bashrc`, `.bash_profile` or `.profile`.
```bash
export PATH=$PATH:$HOME/.local/bin
```

With this we should have our script available. To confirm type:
```bash
sudo guardconf
```
