## handle
handle 在所有的task执行完成后才会被执行,即使被通知了多次也只会执行１次.
handle 常用于重启服务或服务器

## Inventory 文件
可管理的主机集群叫inventory,相关参数:  
ansible_ssh_host　主机名字　SSH目的主机名或IP
ansible_ssh_port　主机SSH端口,默认22  
ansible_ssh_user 默认root 登录用户名  
ansible_ssh_pass none 默认,ssh认证所使用的密码  
ansible_connection   
ansible_ssh_private_key_file  none ssh 认证所使用的私钥  
ansible_shell_type sh 命令所使用的shell  
ansible_python_interpreter 默认/usr/bin/python　主机上的python解释器  
