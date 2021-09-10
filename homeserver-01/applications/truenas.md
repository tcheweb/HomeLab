
## Como virtualizar o Truenas no Proxmox
Este tutorial ensina como instalar discos físicos diretamente na VM do TrueNAS, mantendo a performance da aplicação.

1. identificar os discos
Este comando mostra todos os dispositivos instalados no servidor pelo ID único dos discos.

> `ls /dev/disk/by-id`

Uma vez identificado o disco, copiaremos o ID do disco que desejamos.

2. Incorporando o disco na VM do TruNAS
> `qm set 100 -scsi1 /dev/disk/by-id/ata-ST500DM002-1BD142_W3T6084H`

onde:
- 100 = identificador única da instância no Proxmox
- -scsci1 = identificação do dispositivo que será adicionado, precisa ser incrementado de acordo com o último existente. scsi1, scsi2,etc
- /dev/disk/by-id/ata-ST500DM002-1BD142_W3T6084H = o HD