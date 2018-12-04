Ansible 学习笔记
---
Macos && Linux　原生方法
可以使用对应系统的管理软件进行安装
例如：  
apt-get install ansible  
yum install ansible

或使用python管理pip　进行安装  
pip install ansible

---
ansible.cfg 读取顺序:  
1.　当前目录ansible.cfg  
2.　用户主目录 ~/.ansible.cfg  
3.　/etc/ansible.cfg