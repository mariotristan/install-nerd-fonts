# Install Nerd Fonts Script

An interactive Bash script to **download and install Nerd Fonts on macOS** using [fzf](https://github.com/junegunn/fzf) for selection.  
This script fetches the latest Nerd Fonts directly from the official [Nerd Fonts GitHub releases](https://github.com/ryanoasis/nerd-fonts/releases), ensuring you always get the newest patched fonts.

---

## 📖 What Are Nerd Fonts?
[Nerd Fonts](https://www.nerdfonts.com/) are popular developer-focused fonts that have been patched with a large collection of extra glyphs (icons, symbols, and characters).  
They combine programming-friendly fonts like Hack, Fira Code, JetBrains Mono, and Ubuntu Mono with icons from projects such as Font Awesome, Devicons, Octicons, and more.  
This makes them ideal for use in terminals, code editors, and tools like Neovim, tmux, and powerline prompts.

---

## ✨ Features
- Interactive font selection with **fzf** (multi-select supported).
- Downloads fonts directly from **GitHub releases**.
- Installs `.ttf` files into `~/Library/Fonts` for macOS.
- Color-coded output for better readability.
- Strict error handling (`set -euo pipefail`).

---

## 📦 Dependencies
The script requires:
- `curl` (for fetching release data)
- `fzf` (for interactive selection)
- `unzip` (to extract font archives)
- `brew` (optional, used to install `fzf` if missing)

If `fzf` is not installed, the script will attempt to install it via Homebrew.

---

## 🚀 Usage

1. Clone or download this script:
   ```bash
   git clone https://github.com/your-repo/install-nerd-fonts.git
   cd install-nerd-fonts
   chmod +x install_nerd_fonts.sh

 2. Use TAB to select multiple fonts in the fzf menu, then press ENTER to install.
  ```bash
  ➜ Select the Nerd Fonts you want to install (TAB to select multiple):
    Hack
    FiraCode
    JetBrainsMono
    UbuntuMono
  ```
<img width="1650" height="2108" alt="image" src="https://github.com/user-attachments/assets/a528e4db-8109-41a1-b8d8-fa38fcf678ec" />


⚠️ Notes
* The old homebrew/cask-fonts tap is deprecated. This script installs fonts directly from GitHub.
* To update fonts, simply re-run the script — it will fetch the latest release.
* If you want multiple fonts installed automatically, you can edit the script to pre-select them or run it non-interactively.

📝 Author
• zx0r
• Version: 1.1
• Updated by: Mario Tristán ❤️ Copilot
