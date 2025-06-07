## 🔧 Useful Shell Aliases for Arch Linux + i3 (Web Developer Oriented)

```bash
# 📁 File navigation
alias ..='cd ..'
alias ...='cd ../..'
alias c='clear'
alias ls='ls --color=auto -lah'
alias grep='grep --color=auto'

# 📦 Pacman and AUR helpers
alias update='sudo pacman -Syu'
alias install='sudo pacman -S'
alias remove='sudo pacman -Rns'
alias cleanup='sudo pacman -Rns $(pacman -Qtdq)'  # Remove orphans
alias yays='yay -S'
alias yayr='yay -Rns'
alias yaya='yay -Sua'  # Update AUR packages

# 🐧 System
alias reboot='sudo reboot'
alias poweroff='sudo poweroff'
alias services='systemctl list-units --type=service'
alias top='btm'  # Use `bottom` instead of top (install with pacman)

# 💻 Git
alias gs='git status'
alias ga='git add .'
alias gc='git commit -m'
alias gp='git push'
alias gpl='git pull'
alias gco='git checkout'
alias gl='git log --oneline --graph --all'

# 🌐 Web Development
alias serve='php -S localhost:8000'
alias npmi='npm install'
alias npms='npm start'
alias npmb='npm run build'
alias c='code .'  # VSCode in current dir

# 🖥 i3 / Display Management
alias restart-i3='i3-msg restart'
alias reload-i3='i3-msg reload'
alias xrandr-list='xrandr | grep " connected"'
alias killx='sudo systemctl restart display-manager'

# ⚡️ Quick Project Init (mkdir + git + VSCode)
mkproj() {
  mkdir -p "$1" && cd "$1" && git init && code .
}

# 🚀 Optional replacements (if tools are installed)
alias cat='bat'       # Enhanced `cat`
alias top='btop'       # Better system monitor
alias find='fd'        # Fast `find`
alias rg='ripgrep'     # Fast `grep`
alias sys='neofetch'   # Show system info
```

---

## 🛠 Recommended Tools to Install

To get the most out of these aliases, install:

```bash
sudo pacman -S bat btop fd ripgrep neofetch bottom
yay -S visual-studio-code-bin

