# Acer Nitro 

## Hardware

| Componente | Modelo |
|------------|--------|
| Processador | Intel Core i5-13420H (13ª gen) |
| Placa de vídeo | NVIDIA GeForce RTX |
| Memória RAM | 8GB DDR5 |
| Armazenamento | 512GB SSD NVMe |
| Tela | 15.6" FHD 144Hz |

## Software

| Item | Versão |
|------|--------|
| Distribuição | Arch Linux (rolling) |
| Kernel | 7.0.9-arch1-1 |
| Driver NVIDIA | 595.71.05 |
| CUDA | 13.2 |
| Ambiente gráfico | KDE Plasma (a confirmar versão) |

## Comandos úteis para verificar hardware no Arch

```bash
# Processador
lscpu | grep "Model name"

# GPU
nvidia-smi

# Memória
free -h

# Discos
lsblk

# Temperatura (instalar lm_sensors)
sensors