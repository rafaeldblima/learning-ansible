
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

Comando para checar informação das máquinas
ansible centos1 -m setup

Comando file para criar um arquivo dentro das máquinas, caso ele não exista (modulo file)
ansible all -m file -a 'path=/tmp/test state=touch'

Comando para alterar a permissão de escrita no arquivo, se ele existir (modulo file)
ansible all -m file -a 'path=/tmp/test state=file mode=600'

Comando para copiar arquivos (modulo copy)
ansible all -m copy -a 'src=/tmp/x dest=/tmp/x'

Comando para copiar remoto (modulo copy)
ansible all -m copy -a 'remote_src=yes src=/tmp/x dest=/tmp/y'

Comando para realizar algum comando nas máquinas (modulo command)
ansible all -m command -a 'hostname' -o

command module vem como padrão
ansible all -a 'hostname' -o

Criando arquivo utilizando o modulo command caso ele não exista
ansible all -a 'touch /tmp/test_copy_module creates=/tmp/test_copy_module'

Removendo arquivo caso ele exista, utilizando módulo command
ansible all -a 'rm /tmp/test_copy_module removes=/tmp/test_copy_module'

Removendo com módulo file
ansible all -m file -a 'path=/tmp/test_copy_module state=absent'
