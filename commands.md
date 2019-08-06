
Comando para pingar nas masquinas configuradas
ansible all -m ping

Comando para printar mensagens
ansible all -m debug --args='msg="teste"'

Comando para printar com verbosity
 ansible all -vvv -m debug --args='msg="teste" verbosity=3'

Comando para printar em uma linha só
ansible centos -m ping -o

Comando para listar os hosts de um grupo específico
ansible centos --list-hosts