# RecoverPy

RecoverPy is an advanced tool designed to harness the capabilities of your Linux system for efficient file recovery. Unlike other recovery tools, RecoverPy not only restores deleted files but also recovers overwritten data.

The tool conducts a thorough scan of every block on your partition, allowing you to locate specific strings even within binary files.

## Installation

🐧 **RecoverPy is only available on Linux systems.**
🔴 **Root or sudo access is required for installation.**

### Dependencies

Mandatory dependencies include `grep`, `dd`, and `lsblk`. If you are using a major Linux distribution, these tools are likely already installed.

Optional: To display real-time `grep` progress, you can install `progress`.

To install all dependencies:

- Debian-like: `apt install grep coreutils util-linux progress`
- Arch: `pacman -S grep coreutils util-linux progress`
- Fedora: `dnf install grep coreutils util-linux progress`

### Run with pipx

You can run RecoverPy directly with pipx in an isolated environment without installing it. To install pipx, follow the official documentation. Then, run:

```bash
sudo pipx run recoverpy
```

### Installation from pip

```bash
python3 -m pip install recoverpy
```

### Installation from AUR

```bash
yay -S python-recoverpy
```

## Usage

```bash
python3 -m recoverpy
```

1. Select the system partition containing the lost file.
2. Optionally, you can search in your home partition as an alternative.
3. Enter a concise text string for searching (see tips below for better results).
4. Start the search, and results will appear in the left-hand box.
5. Select a result.
6. Once you've found your file, choose 'Open.'
7. Save the block individually or explore neighboring blocks for additional parts of the file.

## Tips

- Always perform backups before using recovery tools.
- Unmount your partition before initiating any recovery process to prevent alterations to your files.
- When entering a search string:
  - Be concise and choose something unique to your file.
  - Keep it simple; exotic characters may affect results.
  - Recall the last edits made to your file.

When multiple results appear, ensure you've selected the latest version. Explore neighboring blocks to ensure you save the entire file.
