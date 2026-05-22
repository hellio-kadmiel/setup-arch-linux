# 🐧 Arch Linux - Setup e Documentação

[![Arch Linux](https://img.shields.io/badge/Arch_Linux-1793D1?style=for-the-badge&logo=arch-linux&logoColor=white)](https://archlinux.org/)
[![Acer](https://img.shields.io/badge/Acer-83B81A?style=for-the-badge&logo=acer&logoColor=white)](https://www.acer.com/)
[![NVIDIA](https://img.shields.io/badge/NVIDIA-RTX3050-76B900?style=for-the-badge&logo=nvidia&logoColor=white)](https://www.nvidia.com/)
[![KDE Plasma](https://img.shields.io/badge/KDE_Plasma-1D99F3?style=for-the-badge&logo=kde&logoColor=white)](https://kde.org/plasma-desktop/)
[![GitHub](https://img.shields.io/badge/GitHub-Repositório-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/hellio-kadmiel/setup-arch-linux)

Este repositório documenta toda a minha jornada de instalação e configuração do **Arch Linux** no notebook **Acer Nitro V15**, desde a criação do USB bootável até a pós-instalação com **KDE Plasma**, drivers **NVIDIA** e ferramentas de desenvolvimento.

Aqui você encontrará:
- 📚 Documentação passo a passo da instalação manual
- 🐛 Registro de erros e soluções (aprendizados valiosos)
- ⚙️ Scripts e configurações que utilizei
- 🎯 Dicas para hardware específico (Acer + NVIDIA)

---

## 📁 Estrutura do Repositório

```bash
setup-arch-linux/
├── 📄 README.md               # Visão geral (você está aqui)
├── 📁 docs/                   # Documentação completa
│   ├── instalacao/            # Etapas da instalação
│   ├── hardware/              # Configurações do Acer Nitro V15
│   └── pos-instalacao/        # Pós-instalação (KDE, drivers, apps)
├── 📁 erros/                  # Erros e soluções
│   ├── rede/                  # Wi-Fi, DNS, etc.
│   ├── hardware/              # Som, teclado, fans, etc.
│   └── software/              # Stremio, codecs, etc.
├── 📁 scripts/                # Scripts de automação (em breve)
├── 📁 configs/                # Backups de arquivos .conf
└── 📁 assets/                 # Imagens, screenshots (futuro)


# 🐧 Arch Linux - Setup e Documentação do Acer Nitro V15

[![Arch Linux](https://img.shields.io/badge/Arch_Linux-1793D1?style=for-the-badge&logo=arch-linux&logoColor=white)](https://archlinux.org/)
[![Acer](https://img.shields.io/badge/Acer-83B81A?style=for-the-badge&logo=acer&logoColor=white)](https://www.acer.com/)
[![NVIDIA](https://img.shields.io/badge/NVIDIA-RTX3050-76B900?style=for-the-badge&logo=nvidia&logoColor=white)](https://www.nvidia.com/)
[![KDE Plasma](https://img.shields.io/badge/KDE_Plasma-1D99F3?style=for-the-badge&logo=kde&logoColor=white)](https://kde.org/plasma-desktop/)
[![GitHub](https://img.shields.io/badge/GitHub-Repositório-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/hellio-kadmiel/setup-arch-linux)

Este repositório documenta toda a minha jornada de instalação e configuração do **Arch Linux** no notebook **Acer Nitro V15**, desde a criação do USB bootável até a pós-instalação com **KDE Plasma**, drivers **NVIDIA**, **Stremio** e ferramentas de desenvolvimento.

Aqui você encontrará:
- 📚 Documentação passo a passo da instalação manual
- 🐛 Registro de erros e soluções (aprendizados valiosos)
- ⚙️ Scripts e configurações que utilizei
- 🎯 Dicas para hardware específico (Acer + NVIDIA)

---

## 📁 Estrutura do Repositório

    setup-arch-linux/
    ├── 📄 README.md               # Visão geral (você está aqui)
    ├── 📁 docs/                   # Documentação completa
    │   ├── instalacao/            # Etapas da instalação
    │   ├── hardware/              # Configurações do Acer Nitro V15
    │   └── pos-instalacao/        # Pós-instalação (KDE, drivers, apps)
    ├── 📁 erros/                  # Erros e soluções
    │   ├── rede/                  # Wi-Fi, DNS, etc.
    │   ├── hardware/              # Som, teclado, fans, etc.
    │   └── software/              # Stremio, codecs, etc.
    ├── 📁 scripts/                # Scripts de automação (em breve)
    ├── 📁 configs/                # Backups de arquivos .conf
    └── 📁 assets/                 # Imagens, screenshots (futuro)

---

## 🛠️ Tecnologias & Apps Utilizados

| Categoria                 | Tecnologia                     |
|---------------------------|--------------------------------|
| Sistema Operacional       | Arch Linux (rolling)           |
| Ambiente Gráfico          | KDE Plasma                     |
| Gerenciador de Janelas    | KWin                           |
| Gerenciador de Login      | SDDM                           |
| Terminal                  | Konsole (padrão KDE)           |
| Navegador                 | Firefox                        |
| Streaming                 | Stremio                        |
| Drivers NVIDIA            | nvidia-dkms, nvidia-utils      |
| Wi-Fi                     | iwd / NetworkManager           |
| Som                       | PipeWire + WirePlumber         |
| Editor de Código          | VS Code (AUR) / VSCodium       |
| Versionamento             | Git                            |

---

## 🚀 Etapas da Instalação

| Etapa | Descrição                                      | Arquivo                                                                                  |
|-------|------------------------------------------------|------------------------------------------------------------------------------------------|
| 01    | Preparação da mídia (Rufus + ISO)              | [docs/instalacao/01-preparacao-midia.md](docs/instalacao/01-preparacao-midia.md)         |
| 02    | Configuração de rede no terminal (iwctl)       | [docs/instalacao/02-configuracao-rede.md](docs/instalacao/02-configuracao-rede.md)       |
| 03    | Particionamento e instalação base              | [docs/instalacao/03-particionamento.md](docs/instalacao/03-particionamento.md)           |
| 04    | Pós-instalação (KDE, NVIDIA, Stremio)          | [docs/pos-instalacao/01-pos-instalacao.md](docs/pos-instalacao/01-pos-instalacao.md)     |

> ⚠️ **Atenção:** Os problemas enfrentados durante essas etapas estão documentados na pasta [`erros/`](erros/).

---

## 💻 Hardware Específico (Acer Nitro V15 ANV15-51-57WS)

| Componente          | Modelo                            | Status                     |
|---------------------|-----------------------------------|----------------------------|
| Processador         | Intel Core i5-13420H (13ª gen)    | ✅ Funcionando             |
| Placa de vídeo      | NVIDIA GeForce RTX 3050 (6GB)     | ✅ Driver proprietário     |
| Memória RAM         | 8GB DDR5 (expansível)             | ⚠️ Gargalo para VMs/Docker |
| Armazenamento       | 512GB SSD NVMe                    | ✅ Leve e rápido           |
| Tela                | 15.6" FHD 144Hz                   | ✅ Fluido (compositor KDE) |
| Wi-Fi               | iwd / NetworkManager              | ✅ Funcionando             |
| Som                 | PipeWire                          | ✅ Funcionando             |
| Teclado RGB         | openrgb (parcial)                 | ⚠️ Ajuste manual          |

Para mais detalhes, veja: [`docs/hardware/acer-nitro-v15.md`](docs/hardware/acer-nitro-v15.md)

---

## 🐛 Erros Documentados (e soluções)

| Categoria  | Erro                                      | Solução                                                       | Arquivo                                                                                        |
|------------|-------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| 🌐 Rede    | Senha do Wi-Fi não conectava              | Usar `iwctl` com atenção a maiúsculas/minúsculas             | [erros/rede/wifi-senha-errada.md](erros/rede/wifi-senha-errada.md)                             |
| 🎧 Hardware| Som saía no notebook ao invés da TV       | Trocar saída no GNOME Network Displays (ou usar Go2TV)       | *em breve*                                                                                     |
| 📺 Software| Stremio sem áudio na transmissão          | Instalar `fdkaac` e configurar PipeWire                      | *em breve*                                                                                     |

> Quer adicionar um erro? Siga o [template](erros/README.md) e envie um pull request ou abra uma issue.

---

## ⌨️ Comandos Úteis (para consulta rápida)

### Wi-Fi via terminal (iwctl)

    iwctl
    [iwd]# station wlan0 scan
    [iwd]# station wlan0 get-networks
    [iwd]# station wlan0 connect "MinhaRede"
    [iwd]# exit

### Drivers NVIDIA

    sudo pacman -S nvidia nvidia-utils nvidia-settings
    nvidia-smi   # verificar funcionamento

### Codecs de áudio (PipeWire)

    sudo pacman -S pipewire pipewire-pulse wireplumber
    systemctl --user enable --now pipewire pipewire-pulse wireplumber



---

## 📌 Próximos Passos (roadmap)

- [ ] Documentar a configuração completa do **KDE Plasma** (tema, widgets, atalhos)
- [ ] Adicionar script de pós-instalação automatizado (pacotes, configurações)
- [ ] Configurar **backup** dos dotfiles (`.config`, `.bashrc`, etc.)
- [ ] Documentar otimizações de **bateria** (TLP, throttling)
- [ ] Criar um guia de **dual boot** (Arch + Windows, se aplicável)

---

## 🤝 Contribuições

Sugestões, correções ou melhorias são muito bem-vindas!  
Abra uma [issue](https://github.com/hellio-kadmiel/setup-arch-linux/issues) ou envie um pull request.

---

## 📜 Licença

MIT - Sinta-se livre para usar, adaptar e compartilhar.

---

⭐ Se este repositório te ajudou de alguma forma, considere dar uma estrela e fala comigo qualquer duvida!

**Feito com 🐧 e ☕ durante a jornada no Arch Linux.**