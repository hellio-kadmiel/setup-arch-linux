# Erro: Sem vídeo após instalar drivers NVIDIA

## Problema
Após instalar os drivers `nvidia` e reiniciar, o sistema ficava com tela preta (sem sinal de vídeo).

## Causa
Problema com o módulo `nvidia` não carregando corretamente ou conflito com o driver `nouveau`.

## Solução
Adicionei `nvidia_drm.modeset=1` nos parâmetros do kernel e regenerei o initramfs:

    sudo nano /etc/default/grub
    # Em GRUB_CMDLINE_LINUX_DEFAULT, adicione: nvidia_drm.modeset=1
    sudo grub-mkconfig -o /boot/grub/grub.cfg
    sudo mkinitcpio -P

