## pkgtrack
A simple CLI tool to snapshot, compare, and roll back Arch Linux packages.
Perfect for testing new installs without leaving junk behind.

## Installation
```bash
cd ~
git clone https://github.com/tuan-cre/pkgtrack.git
cd pkgtrack
makepkg -si
```
## Usage
```bash
pkgtrack before # Take a snapshot of current packages
pkgtrack after # Show new packages since snapshot
pkgtrack rollback # Remove all new packages
pkgtrack snap <name> # Save diff snapshot under a name
pkgtrack remove <name> # Remove packages from that snapshot
```
## Example
```bash
pkgtrack before
sudo pacman -S neovim
pkgtrack after
pkgtrack snap neovim
pkgtrack remove neovim
```
## Files
Snapshots and diffs are stored in ~/.local/share/pkgtrack/
