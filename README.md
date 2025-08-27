# Guide Custom Parrot OS


## Install all Packets

Clone repo:
```bash
git clone https://github.com/ZakXero/Config_Custom_OS.git ~/Download
```


Install all Packets to need:
```bash
sudo apt install qterminal 7zip neofetch wget git lsd bat neovim locate xclic firefox brave-browser scrub fzf ranger zsh zsh-autosuggestions zsh-syntax-highlighting 
```


## Install Window Manager and Fonts


Install Window Manager MATE or Install MATE on base with formatinng disk.
```bash
sudo apt install mate
```


Install Download and Install Fonts:
```bash
# Create folder
cd /usr/share/fonts
sudo mkdir new_fonts
cd new_fonts

# Download Fonts Hack, Iosevka, NerdFontsSymbolsOnly, JetBrainsMono
wget https://github.com/ryanoasis/nerd-fonts/releases/download/v3.4.0/Hack.zip https://github.com/ryanoasis/nerd-fonts/releases/download/v3.4.0/Iosevka.zip https://github.com/ryanoasis/nerd-fonts/releases/download/v3.4.0/JetBrainsMono.zip https://github.com/ryanoasis/nerd-fonts/releases/download/v3.4.0/NerdFontsSymbolsOnly.zip

# Unzip Fonts in /usr/share/fonts/new_fonts
7z x Hack.zip
7z x NerdFontsSymbolsOnly.zip
7z x Iosevka.zip
7z x JetBrainsMono.zip

# Remove .zip
rm Hack.zip JetBrainsMono.zip NerdFontsSymbolsOnly.zip Iosevka.zip

# Updatedb
sudo updatedb
```


```bash

```



## Configure zsh, install sudo plugin, install Powerlvl10k and configure


```bash
#Install Powerlvl10k
cd ~/
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k
echo 'source ~/powerlevel10k/powerlevel10k.zsh-theme' >>~/.zshrc

# Install zsh-plugin-sudo
cd /usr/share/
sudo mkdir zsh-sudo
cd zsh-sudo
sudo wget https://github.com/ohmyzsh/ohmyzsh/blob/master/plugins/sudo/sudo.plugin.zsh
chmod +x sudo.plugin.zsh

# Copy config zsh and p10k to ~/
cd ~/Downloads
cp ~/Downloads/Zsh_config/.zshrc ~/
cp ~/Downloads/Zsh_config/.p10k.zsh ~/

# Link symbolic root config to user config
ln -f -s /root/.zshrc /home/<user>/.zshrc
ln -f -s /root/.p10k /home/<user>/.p10k.zsh

# Change SHELL default to zsh
usermod --shell /usr/bin/zsh <user>
usermod --shell /usr/bin/zsh <root>

# Copy config Qterminal to file ~/.config/qterminal.org/
cp ~/Downloads/Qterminal_config/qterminal.ini ~/.config/qterminal.org/
```



