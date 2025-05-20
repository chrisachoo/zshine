# ✨ Ultimate Terminal Setup Guide

Make your terminal beautiful, productive, and lightning fast on **Linux**, **macOS**, and **Windows (WSL or native)** using Zsh, Oh My Zsh, plugins, and stunning prompt themes like **Oh My Posh**, **Starship**, and **Powerlevel10k**.

## 🧰 Platforms Covered

- ✅ Linux (Debian-based)
- ✅ macOS (Intel & Apple Silicon)
- ✅ Windows (WSL or Windows Terminal)

## 🐚 1. Install Zsh

### 📦 Linux

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install zsh -y
chsh -s $(which zsh)
```

### 🍏 macOS

```bash
brew install zsh
chsh -s /bin/zsh  # or use $(which zsh)
```

### 🪟 Windows (WSL or Windows Terminal)

- WSL: Use your distro’s package manager (e.g. `apt`) to install Zsh.
- Windows Terminal: Install a Linux distro via WSL and follow Linux steps.

## 🎩 2. Install Oh My Zsh

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## 🔌 3. Install Recommended Plugins

```bash
# Autosuggestions
git clone https://github.com/zsh-users/zsh-autosuggestions \
  ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

# Syntax Highlighting
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git \
  ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

# Fast Syntax Highlighting
git clone https://github.com/zdharma-continuum/fast-syntax-highlighting.git \
  ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/fast-syntax-highlighting

# Autocomplete
git clone --depth 1 https://github.com/marlonrichert/zsh-autocomplete.git \
  ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autocomplete
```

Then edit your `~/.zshrc`:

```zsh
plugins=(
  git
  zsh-autosuggestions
  zsh-syntax-highlighting
  fast-syntax-highlighting
  zsh-autocomplete
)
```

```bash
source ~/.zshrc
```

## 💅 4. Choose a Prompt Theme

#### 🌈 Option A: Powerlevel10k

Powerful and highly customizable Oh My Zsh theme.

```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git \
  ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k
```

Edit `.zshrc`:

```zsh
ZSH_THEME="powerlevel10k/powerlevel10k"
```

Apply:

```bash
source ~/.zshrc
```

> 🧠 First run will launch a config wizard for your prompt. Use arrow keys to choose styles.

Install [Nerd Font](https://www.nerdfonts.com/font-downloads) like **MesloLGS NF** and set it in your terminal:

- iTerm2 (macOS): Preferences → Profiles → Text → Font
- Windows Terminal: `settings.json` → `"fontFace": "MesloLGS NF"`

---

#### 💎 Option B: Oh My Posh (Cross-Platform)

```bash
curl -s https://ohmyposh.dev/install.sh | bash -s
oh-my-posh font install
```

Edit `.zshrc`:

```bash
eval "$(oh-my-posh init zsh --config ~/your-theme-path.omp.json)"
```

> Pick a theme: https://ohmyposh.dev/docs/themes

---

#### 🚀 Option C: Starship

```bash
curl -sS https://starship.rs/install.sh | sh
```

Edit `.zshrc`:

```bash
eval "$(starship init zsh)"
```

Then configure:

```bash
mkdir -p ~/.config
nano ~/.config/starship.toml
```

> Browse configs: https://starship.rs/config/

## 🎨 5. Fonts & Terminal Setup

### 🧠 Required Font: Nerd Fonts

Install [MesloLGS Nerd Font](https://www.nerdfonts.com/font-downloads) and apply it:

- **macOS** (iTerm2): Preferences → Profiles → Text → Font → MesloLGS NF
- **Windows** (Terminal): `"fontFace": "MesloLGS NF"` in settings
- **VS Code**: Add to settings.json:

```json
"terminal.integrated.fontFamily": "MesloLGS NF"
```

## ✅ Final Touch

```bash
source ~/.zshrc
exec zsh
```

## 📚 Reference Links

| Tool          | Description                          | Link                                     |
| ------------- | ------------------------------------ | ---------------------------------------- |
| Oh My Zsh     | Zsh configuration framework          | https://ohmyz.sh/                        |
| Powerlevel10k | Feature-rich Zsh theme               | https://github.com/romkatv/powerlevel10k |
| Oh My Posh    | Prompt theme engine (cross-platform) | https://ohmyposh.dev                     |
| Starship      | Fast, minimal prompt                 | https://starship.rs                      |
| Nerd Fonts    | Fonts with icons                     | https://www.nerdfonts.com                |

## 🎉 All Set!

You're now ready with a terminal setup that's not only **productive** but also **visually stunning** across **Linux**, **macOS**, and **Windows**! 🚀
