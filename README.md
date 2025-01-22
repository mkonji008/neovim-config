### everchanging personal development env

1.  copy contents to `~.config/nvim/`

2.  ensure languages and dependencies are installed.
    depending on the distro the names vary.
    there are several possible distros i use for this env, primarily nixos and void, however, fedora and debian dependencies are also listed (if not to be added).
    several packages are not needed for neovim to function, just part of my dev/ tui workflow and i'd rather just keep it here.
3.  most errors after installing and updating lazyvim can be resolved by combing through `:checkhealth`.
    they will if anything be either missing dependencies or treesitter complaining.
    rerun `:TSUpdate` after fixing any treesitter dependencies and if it's still not showing resolved then perform a `:TSInstall <dockerfile>` (dockerfile as example)
4.  ensure you have a proper nerd font installed and set as default in your terminal of choice.
   
    **my personal favorite fonts**
    
    **cascadia code**
    ```
    https://github.com/ryanoasis/nerd-fonts/releases/download/v3.3.0/CascadiaCode.zip
    ```
    **fira code**
    ```
    https://github.com/ryanoasis/nerd-fonts/releases/download/v3.3.0/FiraCode.zip
    ```
    **geist mono**
    ```
    https://github.com/ryanoasis/nerd-fonts/releases/download/v3.3.0/GeistMono.zip
    ```

### dependencies // 2-ext

**fedora**

1. enable rpm fusion prior, free and nonfree
  ```
  sudo dnf install \
  https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm
  ```
  ```
  sudo dnf install \
  https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
  ```
2. lazygit is available through copr
  ```
  sudo dnf copr enable atim/lazygit -y
  sudo dnf install lazygit
  ```
3. docker
use docker install scripts from dockers website
`https://docs.docker.com/engine/install/fedora/` - just go through pg 1-2

4. package manager installs

note for clipboard manager if you use wayland or xorg. default is xorg
```
neovim ## from the repo is fine
xclip ## or wlclip for wayland
ripgrep
fzf
fd
docker ## use docker install scripts from dockers website
clang
cmake
cl
gcc
libgcc
zig
ld
gem
dlv
luarocks
npm
ansible
distrobox
cargo
rustc
go
hugo
pipx
zoxide
tldr
bat
ranger
exa
yarn
```
