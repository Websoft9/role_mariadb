Ansible Role: mariadb
=========

在CentOS或者Ubuntu服务器上安装和配置 MariaDB 

Requirements
------------

无特殊要求,此 role 需要 root 用户权限,可以在playbook全局加入 `become: yes`,或者如下调用 role:

```
- hosts: database
  roles:
    - role: role_mariadb
      become: yes
```

Role Variables
--------------

下面列出了可用变量和默认值(请参见"defaults/main.yml"):

```
# 支持版本 Centos7/Ubuntu18.04 支持 10.1 10.2 10.3 10.4 Centos8 10.3/10.4

mariadb_version: "10.4"       

# mariadb root 密码
mariadb_root_password: "123456"  

# 新建数据库
mariadb_databases: []
 # - name: example 
  # encoding: utf8mb4

# 新建数据库用户
mariadb_users: []
 # - name: example
  # host: localhost
  # password: password
  # priv: 'example.*:ALL'
```



Dependencies
------------

None

Example Playbook
----------------

```
- hosts: db-servers
  become: yes
  vars_files:
    - vars/main.yml
  roles:
    - { role: role_mariadb }
```

`vars/main.yml` :
```
mariadb_version: "10.4"
mariadb_root_password: "123456" 

mariadb_databases: 
  - name: example 
    encoding: utf8mb4

  
mariadb_users: 
  - name: example
    host: localhost
    password: password
    priv: 'example.*:ALL'
```

License
-------

BSD

