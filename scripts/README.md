# 01 - Pós-instalação

Depois de reiniciar o sistema, ainda estamos no terminal. Agora precisamos configurar o resto.

## Conectar Wi-Fi novamente

    iwctl
    [iwd]# station wlan0 connect "MinhaRede"
    [iwd]# exit

## Criar usuário

    useradd -m -G wheel -s /bin/bash kadimas
    passwd kadimas

## Instalar sudo

    pacman -S sudo
    EDITOR=nano visudo

Descomente a linha:
    %wheel ALL=(ALL:ALL) ALL

## Instalar KDE Plasma

    pacman -S plasma-meta kde-applications-meta

## Instalar SDDM (gerenciador de login)

    systemctl enable sddm
    systemctl start sddm

## Instalar drivers NVIDIA

    pacman -S nvidia nvidia-utils nvidia-settings

## Instalar NetworkManager

    pacman -S networkmanager
    systemctl enable NetworkManager

## Instalar codecs de áudio

    pacman -S pipewire pipewire-pulse wireplumber

## Instalar utilitários

    pacman -S firefox git base-devel

## Resultado

Sistema pronto com KDE Plasma, drivers NVIDIA e Stremio instalado.