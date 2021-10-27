# install-mariadb-ubuntu
```bash
sudo add-apt-repository universe
sudo add-apt-repository multiverse
sudo apt-get -y install mariadb-server mariadb-client
mysql_secure_installation
```

```
#Output
mysql_secure_installation >> Basic Environment for MySQL root
Enter current password for root (enter for none): <-- ให้กด enter
Set root password? [Y/n] <— y
New password: <-- กรอก รหัสผ่าน MariaDB สำหรับ root ลงไป
Re-enter new password: <-- กรอก รหัสผ่าน MariaDB สำหรับ root ซ้ำอีกครั้ง
Remove anonymous users? [Y/n] <— y
Disallow root login remotely? [Y/n] <— y
Reload privilege tables now? [Y/n] <— y
mysql -u root -p >> Test Login Mysql root 
```

```bash
mysql -u root
```

```sql
CREATE USER ‘admin'@'localhost' IDENTIFIED BY Test12345;
GRANT ALL PRIVILEGES ON *.* TO admin@localhost WITH GRANT OPTION;
FLUSH PRIVILEGES;
```
