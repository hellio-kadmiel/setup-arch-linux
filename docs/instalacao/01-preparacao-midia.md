# 01 - Preparação da Mídia e Boot

## 📦 Materiais necessários
- Um pendrive (mínimo 4GB)
- Acesso à internet no computador onde vai criar o USB
- O computador alvo (notebook (no meu caso))

## 🔧 Passo a passo

### 1. Download da ISO
- Acessei o site oficial: https://archlinux.org/download/
- Baixei a ISO mais recente (arquivo com extensão `.iso`)
- Usei um espelho (mirror) próximo ao Brasil para download mais rápido

### 2. Criação do USB bootável com Rufus (no Windows)

| Configuração | Valor escolhido |
|:-------------|:----------------|
| Dispositivo | O pendrive (cuidado para não escolher o HD) |
| Seleção de boot | A ISO do Arch Linux baixada |
| Esquema de partição | **GPT** |
| Sistema alvo | **UEFI (não CSM)** |
| Sistema de arquivos | FAT32 (padrão) |

**Por que GPT + UEFI?** 
- Meu notebook usa UEFI, não o BIOS legado
- O Arch Linux recomenda UEFI para sistemas modernos

### 3. Configuração do BIOS/UEFI no notebook

Antes de bootar pelo pendrive, precisei:
1. Reiniciar o notebook e apertar **F2** (ou **Del**) para entrar na BIOS
2. Desabilitar **Secure Boot** (importante para o Arch)
3. Mudar a ordem de boot para priorizar o USB
4. Salvar e sair (F10)

### 4. Boot no Arch Linux

Com o pendrive conectado, o notebook iniciou direto no menu do Arch, mostrando:
1. Arch Linux
2. Arch Linux (fallback)
3. UEFI Shell