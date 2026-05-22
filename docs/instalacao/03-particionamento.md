# 03 - Particionamento e Instalação Base

## Visão geral
Antes de instalar o Arch, precisei preparar o disco rígido com as partições necessárias. Meu notebook Acer Nitro V15 usa UEFI, então o esquema de partições é diferente do BIOS legado.

## Verificando o disco

    lsblk

Saída:
    nvme0n1 476.9G disk

## Esquema de partições (UEFI)

| Partição | Tamanho | Formato | Montagem |
|----------|---------|---------|----------|
| nvme0n1p1 | 1GB | FAT32 | /boot |
| nvme0n1p2 | 8GB | swap | (swap) |
| nvme0n1p3 | resto | ext4 | /mnt |

## Criar partições com cfdisk

    cfdisk /dev/nvme0n1

Dentro do cfdisk:
- Escolher GPT (para UEFI)
- Criar partição EFI: 1G, tipo `EFI System`
- Criar partição swap: 8G, tipo `Linux swap`
- Criar partição raiz: resto do espaço, tipo `Linux filesystem`
- Clicar em `Write`, digitar `yes`, depois `Quit`

## Formatando

    mkfs.fat -F32 /dev/nvme0n1p1
    mkswap /dev/nvme0n1p2
    mkfs.ext4 /dev/nvme0n1p3

## Montando

    mount /dev/nvme0n1p3 /mnt
    mkdir -p /mnt/boot
    mount /dev/nvme0n1p1 /mnt/boot
    swapon /dev/nvme0n1p2

## Instalar sistema base

    pacstrap -K /mnt base linux linux-firmware

## Gerar fstab

    genfstab -U /mnt >> /mnt/etc/fstab

## Entrar no sistema (chroot)

    arch-chroot /mnt

## Configurações básicas dentro do chroot

Fuso horário:
    ln -sf /usr/share/zoneinfo/America/Sao_Paulo /etc/localtime
    hwclock --systohc

Idioma:
    nano /etc/locale.gen
(descomente a linha: `pt_BR.UTF-8 UTF-8`)
    locale-gen
    echo "LANG=pt_BR.UTF-8" > /etc/locale.conf

Hostname:
    echo "dimas-nitro" > /etc/hostname

Senha do root:
    passwd

## Finalizar e reiniciar

    exit
    umount -R /mnt
    swapoff /dev/nvme0n1p2
    reboot

## Resultado
Sistema base instalado com sucesso.
