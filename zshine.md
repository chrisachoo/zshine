# 🚀 Ultimate Linux Terminal Setup Guide

Transform your terminal into a powerful and visually stunning development environment using **Zsh**, **Oh My Zsh**, **plugins**, and **Oh My Posh**.

---

## 🛠️ Prerequisites

- A Debian-based Linux system (e.g., Ubuntu)
- Internet connection
- Access to the terminal

---

## 1. 🐚 Install Zsh

Zsh is an advanced shell with powerful features compared to the default Bash shell.

```bash
# Update package lists
sudo apt update

# Upgrade all current packages
sudo apt upgrade -y

# Install Zsh
sudo apt install zsh -y

# Set Zsh as the default shell
chsh -s $(which zsh)
```

> **ℹ️ Note**: Log out and log back in (or reboot) for the shell change to take effect.

---

## 2. 🎩 Install Oh My Zsh

[Oh My Zsh](https://ohmyz.sh) is a delightful framework for managing your Zsh configuration.

```bash
# Download and run the Oh My Zsh installer script
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

---

## 3. 🔌 Install Zsh Plugins

These plugins enhance your terminal with suggestions, highlighting, and advanced autocomplete.

### ➕ Autosuggestions

Suggests commands as you type based on history.

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions
```

### 🎨 Syntax Highlighting

Colorizes commands to make it easier to spot errors.

```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
```

### ⚡ Fast Syntax Highlighting

A faster and more feature-rich syntax highlighter.

```bash
git clone https://github.com/zdharma-continuum/fast-syntax-highlighting.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/fast-syntax-highlighting
```

### 🔍 Autocomplete

Provides smarter and faster tab completions.

```bash
git clone --depth 1 -- https://github.com/marlonrichert/zsh-autocomplete.git $ZSH_CUSTOM/plugins/zsh-autocomplete
```

---

## 4. 💅 Install Oh My Posh

[Oh My Posh](https://ohmyposh.dev) provides beautiful and customizable prompts.

### 🧪 Install Oh My Posh

```bash
# Install Oh My Posh
curl -s https://ohmyposh.dev/install.sh | bash -s
```

### 🔠 Install Nerd Fonts

Fonts required for displaying icons and glyphs correctly.

```bash
oh-my-posh font install
```

> **📌 Tip**: Restart your terminal or select the installed Nerd Font in your terminal emulator settings.

---

## 5. 🧾 Configure Your Terminal

### 🖼️ Set Oh My Posh Theme

Pick a theme from [Oh My Posh Themes](https://github.com/JanDeDobbeleer/oh-my-posh/tree/main/themes) and use it in your `.zshrc`.

```bash
# Example: Use the Tokyonight Storm theme
echo 'eval "$(oh-my-posh init zsh --config ~/JanDeDobbeleer/tokyonight_storm.omp.json)"' >> ~/.zshrc
```

Then apply changes:

```bash
source ~/.zshrc
# or restart shell
exec zsh
```

### 🧩 Enable Zsh Plugins

Edit your `.zshrc` to enable the plugins:

```bash
nano ~/.zshrc
```

Find the line:

```bash
plugins=(git)
```

Replace with:

```bash
plugins=(
  git
  zsh-autosuggestions
  zsh-syntax-highlighting
  fast-syntax-highlighting
  zsh-autocomplete
)
```

Save and exit, then apply the changes:

```bash
source ~/.zshrc
```

---

## 6. 🖥️ Optional: Configure VS Code Terminal

To ensure icons and fonts render correctly in VS Code:

1. Open VS Code
2. Press `Ctrl + ,` to open settings
3. Search for `terminal.integrated.fontFamily`
4. Add the following:

```json
{
  "terminal.integrated.fontFamily": "MesloLGM Nerd Font"
}
```

---

## 🎉 Done! Enjoy Your Terminal

You've successfully set up a powerful, beautiful, and highly functional Linux terminal environment.

---

## 📚 Reference

- Plugin source list: [GitHub Gist by @n1snt](https://gist.github.com/n1snt/454b879b8f0b7995740ae04c5fb5b7df)
- [Oh My Zsh](https://ohmyz.sh/)
- [Oh My Posh](https://ohmyposh.dev)
- [Nerd Fonts](https://www.nerdfonts.com/)
