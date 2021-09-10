# PROXMOX Configuration #

Version: **7.0-8**

Hostname: **homeserver-01**   
IP: **192.168.0.10:8006**  
Gateway: **192.168.0.1**

## Padrões de ID para VM´s ##
- 100-199 - VM´s de Produção  
- 200-299 - VM´s de Teste
- 300-399 - Containers LXC


O primeiro passo após a instalação bem sucedida do Proxmox é acessar o console e verificar se o sistema precisa de atualizações.

**Atualizar o sistema**  
Executar os comandos abaixo para buscar atualizações e atualizar o sistema.
> `apt update`  
`apt upgrade`

Após o fim da atualização é aconselhável a reinicialização do sistema.

**Adicionar Imagens ISO**

Este passo pode ser feito via FTP. para isso conecte ao servidor e salve os arquivos em `/var/lib/vz/template/iso`
A segunda opção é fazer o upload pelo próprio painel do Proxmox

Anexar discos KVM a uma instância.

**No prompot do servidor**

qm importdisk `Id da Intância` `nome do arquivo .qcow2` `storage onde ficará o arquivo`

Exemplo:
qm importdisk 206 haos_ova-6.3.qcow2 dados-01
