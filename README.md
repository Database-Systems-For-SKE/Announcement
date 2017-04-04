# Planning-Design

|Link|Description|
|----|-----------|
| [139.59.96.74](https://139.59.96.74) |raw ip address (use for `ssh`) |
| [kamontat.me](https://kamontat.me) | Main website (should always map to `https`) |
| [kamontat.me/phpmyadmin/](https://kamontat.me/phpmyadmin/) | phpmyadmin site |

# how to

## ssh
- type `ssh root@139.59.96.74` on UNIX System (macOS and Linux) 
- use **third party** to done it (windowOS)

# Password Announcement
1. ssh - use this (link)[http://www.md5online.org/md5-encrypt.html] to encrypt my given raw password
2. phpmyadmin - user should be `root` and password will stay at `~/.digitalocean_password`

# Error

## 2002
2002 - No such file or directory<br />The server is not responding (or the local server's socket is not correctly configured).

try to run this script (on `ssh`)
```Bash
  sudo mkdir -p /var/run/mysqld
  sudo chown mysql /var/run/mysqld/
  sudo service mysql restart
```
<small>http://serverfault.com/questions/305053/mysqld-sock-doesnt-exist</small>
