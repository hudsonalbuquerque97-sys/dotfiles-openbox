# Dotfiles Openbox

Configurações pessoais do Openbox para meu setup.

## Conteúdo
- **Openbox**:`rc.xml`, `menu.xml` e autostart.
- **conky arquivo de configuração personalizado
- **polybar arquivo de configuração personalizada
- **scrot-notify

## Requisitos para usar esses dotfiles ## Dependências

Certifique-se de instalar os seguintes pacotes antes de aplicar os dotfiles:

sudo apt install \
  openbox obconf lxappearance lxappearance-obconf \
  dmenu rofi conky-all suckless-tools scrot \
  fonts-font-awesome polybar feh libnotify-bin perl build-essential \
  alacritty geany dunst ranger perl perl-modules build-essential \
  cpanminus git libxml-simple-perl libgtk2-perl libglib-perl

## Instalando obmenu-generator via CPAN direto do git 
sudo cpanm Linux::DesktopFiles Data::Dump
git clone https://github.com/trizen/obmenu-generator.git
cd obmenu-generator
sudo cp obmenu-generator /usr/bin/
sudo chmod +x /usr/bin/obmenu-generator
mkdir -p ~/.config/obmenu-generator
cp schema.pl ~/.config/obmenu-generator/
obmenu-generator -p -i

## Clonando os dotfiles do openbox
# Clona o repositório de configuração diretamente na pasta dotfiles-openbox dentro do HOME
git clone https://github.com/hudsonalbuquerque97-sys/dotfiles-openbox.git
# Cria as pastas se não existirem
mkdir -p ~/.config/openbox ~/.config/conky ~/.config/polybar ~/.local/bin
# Copia as configurações
cp -r "$HOME/dotfiles-openbox/.config/openbox/"* ~/.config/openbox/
cp -r "$HOME/dotfiles-openbox/.config/conky/"*   ~/.config/conky/
cp -r "$HOME/dotfiles-openbox/.config/polybar/"* ~/.config/polybar/
# Copia o script scrot-notify
cp "$HOME/dotfiles-openbox/.local/bin/scrot-notify" ~/.local/bin/
chmod +x ~/.local/bin/scrot-notify

## Instalação completa ##




