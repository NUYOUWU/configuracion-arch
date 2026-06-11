# Install Nuyo Arch

Mannual personal para reconstruir mi entorno Arch Linux.

## 1. Instalar paquetes base

```bash
sudo pacman -S --needed git base-devel


clonar configuracion

git clone https://github.com/NUYOUWU/configuracion-arch.git ~/nuyo-arch

restaurar scripts

mkdir -p ~/.local/bin
cp ~/nuyo-arch/bin/* ~/.local/bin/
chmod +x ~/.local/bin/*

restaurar configuraciones
mkdir -p ~/.config
cp -r ~/nuyo-arch/config/hypr ~/.config/
cp -r ~/nuyo-arch/config/waybar ~/.config/
cp -r ~/nuyo-arch/config/wofi ~/.config/

instalar paquetes guardados

sudo pacman -S --needed - < ~/nuyo-arch/packages/pacman-explicit.txt

cat ~/nuyo-arch/system/enabled-services.txt
```
