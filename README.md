# Домашнее задание к занятию «Система мониторинга Zabbix» - `Костюк Денис`

### Задание 1
#### Требования к результаты 

1. Прикрепите в файл README.md скриншот авторизации в админке
   ![Скрин1](https://github.com/denniskostyuk/zabbix-1/blob/main/screen-11.png)
   ![Скрин2](https://github.com/denniskostyuk/zabbix-1/blob/main/screen-12.png)
   ![Скрин3](https://github.com/denniskostyuk/zabbix-1/blob/main/screen-13.png)
   
2. Приложите в файл README.md текст использованных команд в GitHub

sudo su
apt install postgresql
apt update
apt upgrade
wget https://repo.zabbix.com/zabbix/6.0/debian/pool/main/z/zabbix-release/zabbix-release_6.0-4+debian11_all.deb
dpkg -i zabbix-release_6.0-4+debian11_all.deb
apt update
apt install zabbix-server-pgsql zabbix-frontend-php php7.4-pgsql zabbix-apache-conf zabbix-sql-scripts
systemctl status zabbix-server.service
sudo -u postgres createuser --pwprompt zabbix
sudo -u postgres createdb -O zabbix zabbix
zcat /usr/share/zabbix-sql-scripts/postgresql/server.sql.gz | sudo -u zabbix psql zabbix
nano /etc/zabbix/zabbix_server.conf
systemctl restart zabbix-server apache2
systemctl enable zabbix-server apache2
systemctl status zabbix-server.service

### Задание 2
