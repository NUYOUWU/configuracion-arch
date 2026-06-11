# Install Nuyo Arch

Mannual personal para reconstruir mi entorno Arch Linux.

## 1. Instalar paquetes base

```bash
sudo pacman -S --needed git base-devel
```

clonar configuracion
```bash
git clone https://github.com/NUYOUWU/configuracion-arch.git ~/nuyo-arch
```
restaurar scripts
```bash
mkdir -p ~/.local/bin
cp ~/nuyo-arch/bin/* ~/.local/bin/
chmod +x ~/.local/bin/*
```
restaurar configuraciones
```bash
mkdir -p ~/.config
cp -r ~/nuyo-arch/config/hypr ~/.config/
cp -r ~/nuyo-arch/config/waybar ~/.config/
[ -d ~/nuyo-arch/config/wofi ] && cp -r ~/nuyo-arch/config/wofi ~/.config/
```
instalar paquetes guardados

```bash
sudo pacman -S --needed - < ~/nuyo-arch/packages/pacman-explicit.txt
cat ~/nuyo-arch/system/enabled-services.txt
```
