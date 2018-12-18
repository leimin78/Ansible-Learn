PlayBook  
---
剧本,yml的脚本程序 ansible会按yml脚本去到指定机器执行相关task  
代码示例-ubuntu-nginx安装示例:
    - name: configure webserver with nginx
    - hosts: mynode
    - sudo: True
    - tasks:
          - name: install nginx
            apt: name=nginx update_cache=yes
          
          - name: copy nginx config file
            copy: src=files/nginx.conf dest=/etc/nginx/conf.d

          - name: copy index.html
            template: src=template/index.html.j2 dest=/usr/share/nginx/html/index.html mode=0644
          - name: restart nginx
            service: name=nginx state=restarted

一个json文件必定是一个合法的yaml文件.  
playbook:最小执行条件  
1.一组hosts  
2.一组task

---
常见变量  
1.name 任务描述  
2.sudo 是否已root权限执行  
3.vars 变量与其值组成的类型  

不同的模块帮助命令查看例如:   
ansible-doc apt   

---
playbook,play,host,task,module　关系

playbook <-- play <-- host  
||  
task --> module 