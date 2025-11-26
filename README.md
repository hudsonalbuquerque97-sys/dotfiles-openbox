# Dotfiles Openbox

![Linux Mint](https://img.shields.io/badge/Linux%20Mint-20.3-%2387CF3E?logo=linuxmint&logoColor=white)
![Openbox](https://img.shields.io/badge/Openbox-Window_Manager-blue?logo=openbox&logoColor=white)
![Dotfiles](https://img.shields.io/badge/Dotfiles-Openbox_on_Linux_Mint-6A9B78?logo=linux&logoColor=white)
![Dotfiles](https://img.shields.io/badge/Dotfiles-Config_Files-blueviolet?logo=gnu&logoColor=white)
![Neovim](https://img.shields.io/badge/Neovim-Config-%2357A143?logo=neovim&logoColor=white)
![Bash](https://img.shields.io/badge/Shell-Bash-4EAA25?logo=gnu-bash&logoColor=white)
![Git](https://img.shields.io/badge/Git-dotfiles-%23F05032?logo=git&logoColor=white)

---

Configurações pessoais do Openbox para meu setup no linux mint.

## Conteúdo
- **Openbox**:`rc.xml`, `menu.xml` e autostart.
- **conky arquivo** de configuração personalizado
- **polybar arquivo** de configuração personalizada
- **script scrot-notify**

## Requisitos para usar esses dotfiles 

Dependências Certifique-se de instalar os seguintes pacotes antes de aplicar os dotfiles:

```bash
sudo apt install \
  openbox obconf lxappearance lxappearance-obconf \
  dmenu rofi conky-all suckless-tools scrot \
  fonts-font-awesome polybar feh libnotify-bin perl build-essential \
  alacritty geany dunst ranger perl perl-modules build-essential \
  cpanminus git libxml-simple-perl libgtk2-perl libglib-perl
```

## Instalando obmenu-generator via CPAN direto do git

```bash
sudo cpanm Linux::DesktopFiles Data::Dump \
git clone https://github.com/trizen/obmenu-generator.git \
cd obmenu-generator \
sudo cp obmenu-generator /usr/bin/ \
sudo chmod +x /usr/bin/obmenu-generator \
mkdir -p ~/.config/obmenu-generator \
cp schema.pl ~/.config/obmenu-generator/ \
obmenu-generator -p -i 
```

## Clonando os dotfiles do openbox

## Clona o repositório de configuração diretamente na pasta dotfiles-openbox dentro do HOME

```bash
git clone https://github.com/hudsonalbuquerque97-sys/dotfiles-openbox.git 
```

## Cria as pastas se não existirem 

```bash
mkdir -p ~/.config/openbox ~/.config/conky ~/.config/polybar ~/.local/bin 
```

## Copia as configurações

```bash
cp -r "$HOME/dotfiles-openbox/.config/openbox/"* ~/.config/openbox/ \
cp -r "$HOME/dotfiles-openbox/.config/conky/"*   ~/.config/conky/ \
cp -r "$HOME/dotfiles-openbox/.config/polybar/"* ~/.config/polybar/
``` 
## Copia o script scrot-notify

```bash
cp "$HOME/dotfiles-openbox/.local/bin/scrot-notify" ~/.local/bin/ \
chmod +x ~/.local/bin/scrot-notify 
```
## Instalação completa ##

Screenshot 

![Minha área de trabalho](https://raw.githubusercontent.com/hudsonalbuquerque97-sys/dotfiles-openbox/refs/heads/master/2025-09-04-161217.png)
