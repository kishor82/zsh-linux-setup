## Zsh (Oh My ZSH) setup and theme installation for Linux
- Install Zsh - `sudo apt install zsh` 
- Test if we are using ZSH and the correct ZSH - ` which zsh`
- Install “Oh My ZSH” 
 `sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
`
- Installing “agnoster” Oh My ZSH theme
1. Install Powerline fonts
    - `git clone https://github.com/powerline/fonts.git`
    - `cd fonts`
    - `./install.sh`
2. Change the Theme to “agnoster”
 - `nano ~/.zshrc`
 - Set `ZSH_THEME="agnoster"` and save the file
3.  Set Powerline font
- Open `ITerm2 > Preferences > Profile Name > Text > Custom font` 
- And set it to something that has “for Powerline”. I’m choosing “Meslo LG DZ for Powerline” font.

#  Add Syntax Highlighting Plugin
The Syntax Highlighting plugin adds beautiful colors to the commands you are typing.
- Clone the zsh-syntax-highlighting plugin’s repo and copy it to the “Oh My ZSH” plugins directory.
- `git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting`
- Activate the plugin in ~/.zshrc by adding `zsh-syntax-highlighting to the Plugins section as shown below.
```bash
plugins=(git zsh-syntax-highlighting)
```
- Re-read zshrc configuration - `source ~/.zshrc`

#  Add ZSH-AutoSuggestion Plugin
- This plugin auto suggests any of the previous commands.
- `git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions`
-Activate the plugin in ~/.zshrc by adding `zsh-syntax-highlighting to the Plugins section as shown below.
```bash
plugins=(git zsh-syntax-highlighting zsh-autosuggestions)
```

- Hide computer name in terminal :  add `export DEFAULT_USER=$USER` to .zshrc 

