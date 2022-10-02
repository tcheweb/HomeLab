# PROCEDIMENTO PADRÃO PARA CRIAÇÃO DE INSTÂNCIAS NO UBUNTU #

## Durante a Instalação ##

1. configurar IP Fixo**
    subnet: 192.168.0.0/24

    DNS
        187.44.80.2
        187.44.90.2



2. Habilitar SSH Server**

## Pós instalação ##
1. Configurar o timez1. one
> `$ sudo timedatectl set-timezone America/Sao_Paulo`

2. Atualizar o sistema.
> `sudo apt update`  
`sudo apt upgrade`

3. Reiniciar


3. Instalar o Qemu para ter mais informações sobre a instância no Proxmox
- Habilitar nas configurações da intância em Options o Qemu
- Instalar o pacote na instância
> `sudo apt-get install qemu-guest-agent`  

Reiniciar a instância

