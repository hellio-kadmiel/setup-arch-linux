# 02 - Configuração de Rede via Terminal

## 🌐 Contexto
Após bootar pelo pendrive, o Arch Linux inicia sem interface gráfica. Para instalar qualquer pacote, é preciso estar conectado à internet.

Meu notebook Acer Nitro V15 tem apenas conexão Wi-Fi (sem cabo de rede), então precisei configurar pelo terminal.

## 🔍 Descobrindo o nome da interface Wi-Fi

```bash
ip link
Saída no meu notebook:
1: lo: ...
2: wlan0: ...
```  

## 📝 Conectando com iwctl pelo método oficial
   
# Dentro do iwctl:
1. [iwd]# device list
2. [iwd]# station wlan0 scan
3. [iwd]# station wlan0 get-networks
4. [iwd]# station wlan0 connect "SuaRedeWiFi"
# Digitar a senha quando solicitado

## Verificar conexão com a internet
1. [iwd]# station wlan0 show
2. [iwd]# exit

### Validando a conexão

Depois de conectar, testei se a internet estava realmente funcionando:

```bash
# Teste 1: ping para um IP conhecido (Google DNS)
ping 8.8.8.8