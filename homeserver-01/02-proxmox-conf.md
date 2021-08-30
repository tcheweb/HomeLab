# PROXMOX Configuration #

Version: **7.0-8**

Hostname: **homeserver-01**   
IP: **192.168.0.10:8006**  
Gateway: **192.168.0.1**

## Padrões de ID para VM´s ##
- 100-199 - VM´s de Produção  
- 200-299 - VM´s de Teste

-----


O primeiro passo após a instalação bem sucedida do Proxmox é acessar o console e verificar se o sistema precisa de atualizações.

**Atualizar o sistema**  
Executar os comandos abaixo para buscar atualizações e atualizar o sistema.
> `apt update`  
`apt upgrade`

Após o fim da atualização é aconselhável a reinicialização do sistema.

**Adicionar Imagens ISO**

Conectar ao servidor via FTP e salvar as imagens ISO em `/var/lib/vz/template/iso`


## Adicionar Discos ##



## Ativar o qemu nas VM´s


