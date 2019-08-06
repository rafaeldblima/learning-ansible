
Comando para pingar nas masquinas configuradas
ansible all -m ping

Comando para printar mensagens
ansible all -m debug --args='msg="teste"'

Comando para printar com verbosity
 ansible all -vvv -m debug --args='msg="teste" verbosity=3'