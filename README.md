# Zsh Config
This is how to configure zsh or config that I currently use. <br>
Why using zsh? This is the reason why I like my terminal and not make me bored when using it.
1. Colorfull
2. More icon
3. Auto suggestion

### Intall ZSH
Some linux distribution come with zsh by default but some distribution not such as Arch Linux,
so here is my step by step that I use to install and set the zsh as my default shell
and `I use arch btw` hehehe

```sudo pacman -Sy zsh```

### Set ZSH as default shell
Because Arch Linux comes with bash as the default shell we need to change it to zsh.
```chsh -s $(which zsh)```

### Install the zsh plugin manager
In this case, I use zinit as zsh plugin manager to manage the zsh plugin. <br> 
[Check the repository](https://github.com/zdharma-continuum/zinit)
1. Auto install run this <br>
 ```
 bash -c "$(curl --fail --show-error --silent --location https://raw.githubusercontent.com/zdharma-continuum/zinit/HEAD/scripts/install.sh)"
 ```
2. Restart your shell (close and open again) or run → source .zshrc
3. Try self update by run <br>
```zinit self-update```

### Install theme
I use power10k theme in this case, [here the link](https://github.com/romkatv/powerlevel10k) <br>
1. Auto install, run from shell
    ```
    zinit ice depth "1"
    zinit light romkatv/powerlevel10k
    ```
    the depth command is use to determine the git clone depth
2. Manual install
    If the auto install doesn't work, need to add this manually to .zshrc
   `zinit ice depth=1; zinit light romkatv/powerlevel10k`
3. Restart your shell (close and open again) or run → source .zshrc
4. Configure theme
    `p10k configure`
   and follow the step by answering the question. <br>
   **Note**: my be you'll need to install [nerdfont](https://www.nerdfonts.com/)

### Install plugin
1. Plugin history-search-multi-word loaded with investigating.
   `zinit load zdharma-continuum/history-search-multi-word`
2. Auto suggestion
   `zinit light zsh-users/zsh-autosuggestions`
3. Syntax highlighting
   `zinit light zdharma-continuum/fast-syntax-highlighting`

### Still not sure
Can compare your zshrc with mine in this repository.

## Tada! Your Terminal Not Boring Anymore.
