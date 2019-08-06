Challenge

1. Use the file module to create a file on the remote host called '/tmp/test_modules.txt' with permissions 600
R = ansible centos1 -m file -a 'path=/tmp/test_modules.txt state=touch mode=600'

2. Using the fetch module, copy the file from the remote, to the local
R = ansible centos1 -m fetch -a 'src=/tmp/test_modules.txt dest=/tmp/test_modules.txt'