
Comando para pingar nas masquinas configuradas
ansible all -m ping

Comando para printar mensagens
ansible all -m debug --args='msg="teste"'

Comando para printar com verbosity (verbosity = quantidade de v)
 ansible all -vvv -m debug --args='msg="teste" verbosity=3'

Comando para printar em uma linha só (-o)
ansible centos -m ping -o

Comando para listar os hosts de um grupo específico
ansible centos --list-hosts

Comando para informar um inventory customizado (-i)
ansible all -i hosts.yml -m ping -o

Comando para informar uma variável de ambiente diferente (-e)
ansible linux -m ping -e 'ansible_port=22' -o
