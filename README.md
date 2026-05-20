# 🐧 Diário da Minha Jornada no Arch Linux

Este repositório foi criado com o objetivo de documentar os meus estudos práticos em sistemas operativos, infraestrutura e administração de sistemas (SysAdmin). Aqui registo todo o processo, desde a criação do (boot) até à pós-instalação e análise de hardware.

---

## 🛠️ Etapa 1: A Instalação 100% Manual
### 1. Preparação da Mídia e Boot
* **Download:** Obtenção da imagem ISO oficial diretamente do site do Arch Linux.
* **Criação do USB:** Utilização do utilitário **Rufus** para gravar a ISO num pendrive, utilizando a tabela de partições GPT e o modo UEFI.

### 2. Configuração de Rede via Terminal
O primeiro grande desafio foi estabelecer ligação à Internet sem qualquer interface gráfica, utilizando apenas o terminal:
* Utilização do utilitário `iwctl` (iwd) para gerir o Wi-Fi do portátil.
* Comandos executados para pesquisar as redes e efetuar a autenticação:
  ```bash
  device list
  station wlan0 scan
  station wlan0 get-networks
  station wlan0 connect "Nome_Da_Rede"
---
  Validação da conectividade através do comando "ping google.com."

### 3.Particionamento e Instalação Base
Esquema de Partições: Criação manual das partições necessárias utilizando ferramentas como o cfdisk (partição EFI para o boot, partição Swap para gestão de memória e partição Raiz / para o sistema).

 * Formatação: Aplicação dos sistemas de ficheiros adequados (FAT32 para o EFI e EXT4 para o sistema principal).

* Instalação do Core: Utilização do comando pacstrap para instalar o sistema base, o kernel Linux e os firmwares necessários (linux-firmware).

* Configuração Interna (Chroot): Entrada no sistema instalado através de arch-chroot para configurar o fuso horário, idioma (locale), nome da máquina (hostname) e definição das palavras-passe.
