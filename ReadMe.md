#  Резервное копирование с помощью утилиты Borg


Цель домашнего задания
Научиться настраивать резервное копирование с помощью утилиты Borg






### 1.Настроим стенд Vagrant с двумя виртуальными машинами: backup_server и client.

[Vagrantfile](Vagrantfile)

![текст](screenshots/vagrant_status.png)  



### 2.Пишем plaubook

[playbook](playbook.yml)



__Устанавливаем на client и backup сервере borgbackup__
![текст](screenshots/install_borg.png)  



__На сервере backup создаем пользователя и каталог /var/backup и назначаем на него права пользователя borg__  
![текст](screenshots/create_user.png)  



__На сервер backup создаем каталог ~/.ssh/authorized_keys в каталоге /home/borg__
![текст](screenshots/sshd.png)  



__На клиенте создаем и копируем ssh key__
![текст](screenshots/ssh_key.png)  






```php
docker commit 1e6229dd21rd nginxnew:v1.2
```
