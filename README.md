<div align="right">
  
[![LANG](https://github.com/user-attachments/assets/a6722ae9-602a-4a2f-ab85-6f76d4ac0b51)](README.es.md)
<div align="right">
Switch Language
</div>
</div>

# Guardconf

**Guardconf** is a script designed to simplify the configuration and management of WireGuard peers. It allows you to add new peers to your WireGuard configuration file and generate the necessary public and private keys for these peers.

---

## Installation

Follow these steps to install and set up **Guardconf** on your system.

### 1. Download the Script

You can download the script using either `curl` or `wget`.

#### Using `curl`:
```bash
curl -o guardconf https://raw.githubusercontent.com/loadept/guardconf/refs/heads/master/bin/guardconf
```

#### Using `wget`:
```bash
wget -O guardconf https://raw.githubusercontent.com/loadept/guardconf/refs/heads/master/bin/guardconf
```

---

### 2. Assign Execution Permissions

Make the script executable by running:
```bash
chmod +x guardconf
```

---

### 3. Move the Script to Your PATH

To run **Guardconf** from anywhere on your system, move it to a directory that is included in your `PATH`. For user-specific convenience, we recommend using `~/.local/bin`.

#### Create the Directory (if it doesn't exist):
```bash
mkdir -p ~/.local/bin
```

#### Move the Script:
```bash
mv ./guardconf ~/.local/bin/
```

---

### 4. Ensure `~/.local/bin` is in Your PATH

Check if `~/.local/bin` is already in your `PATH`:
```bash
echo $PATH
```

If you see something like `:/home/your-username/.local/bin`, it means the directory is already included.

#### If Not, Add It to Your PATH:

Add the following line to your shell configuration file (e.g., `.bashrc`, `.bash_profile`, or `.profile`):
```bash
export PATH=$PATH:$HOME/.local/bin
```

Then, reload your shell configuration:
```bash
source ~/.bashrc  # or source ~/.bash_profile, depending on your setup
```

---

### 5. Verify Installation

To confirm that **Guardconf** is installed correctly, run:
```bash
guardconf
```

If the script runs without errors, the installation is successful.

---

## Usage

Once installed, you can use **Guardconf** to manage your WireGuard configuration. For example, to add a new peer, run:
```bash
sudo guardconf
```

Follow the on-screen prompts to configure your WireGuard peers.

---

## Notes

- Ensure you have `sudo` privileges to modify WireGuard configuration files.
- The script is designed to be user-friendly and requires minimal manual intervention.

---

## Troubleshooting

- **Script Not Found**: If the `guardconf` command is not recognized, ensure `~/.local/bin` is in your `PATH` and the script is executable.
- **Permission Denied**: If you encounter permission issues, try running the script with `sudo`.

---

## Contributing

If you'd like to contribute to **Guardconf**, feel free to submit issues or pull requests on the [GitHub repository](https://github.com/loadept/guardconf).
