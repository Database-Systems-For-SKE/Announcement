# Latest Announment

> 4 teams are created
1. [Design](#Design)
2. [Frontend](#frontend)
3. [Backend](#backend)
4. [Tester](#tester)

### Design
Q: What you do?  
A: design frontend (maybe database association)

Q: What permission you have?  
A: Read Frontend Project (`Read` Premission)

### Frontend
Q: What you do?  
A: frontend development (web and front api)

Q: What permission you have?  
A: Full access to Frontend Project (`Admin` Premission)

### Backend
Q: What you do?  
A: design backend (include api, json parse and database model)

Q: What permission you have?  
A: Full access to Backend Project (`Admin` Premission)

### Tester
Q: What you do?  
A: test all possible, to find out any kind of bug have to fix

Q: What permission you have?  
A: Read both Frontend and Backend Project (`Read` Premission)

--------------------

# Web description

| Link                                                       | Description                                 |
|------------------------------------------------------------|---------------------------------------------|
| [139.59.96.74](https://139.59.96.74)                       |raw ip address (use for `ssh`)               |
| [kamontat.me](https://kamontat.me)                         | Main website (should always map to `https`) |
| [api.kamontat.me](https://api.kamontat.me)                 | API/Backend page for connection to database |
| [kamontat.me/phpmyadmin/](https://kamontat.me/phpmyadmin/) | phpmyadmin site                             |

# how to

## ssh
- type `ssh root@139.59.96.74` on UNIX System (macOS and Linux) 
- use **third party** to done it (windowOS)

# Password Announcement
1. ssh - use this [link](http://www.md5online.org/md5-encrypt.html) to encrypt my given raw password
2. other password you can found at `~/.password`

# Important 

Passwordless via `ssh` (to debug)
1. open terminal
2. exec `cd ~/.ssh`
3. exec `ssh-keygen -b 1024 -t rsa -f id_rsa -P ""`
4. exec `cat id_rsa.pub`
5. exec [ssh](#ssh) command
6. exec `vim ~/.ssh/authorized_keys`
7. append result from **step4**
8. exec `exit`
9. try to [ssh](#ssh) again (and this time program will no asking for password)

via1: https://coolestguidesontheplanet.com/make-passwordless-ssh-connection-osx-10-9-mavericks-linux/  
via2: https://www.cyberciti.biz/tips/linux-multiple-ssh-key-based-authentication.html

--------------------

# Error
### 2002
2002 - No such file or directory<br />The server is not responding (or the local server's socket is not correctly configured).
try to run this script (on `ssh`)
```Bash
  sudo mkdir -p /var/run/mysqld
  sudo chown mysql /var/run/mysqld/
  sudo service mysql restart
```
<small>http://serverfault.com/questions/305053/mysqld-sock-doesnt-exist</small>

### can't open phpmyadmin
- the port might appear, all you need just delete the port (`:80`)

--------------------

# Knowledge
1. ssh `1 user multiple servers`
    - http://serverfault.com/questions/221760/multiple-public-keys-for-one-user
2. ssh `multiple user 1 server`
    - https://www.cyberciti.biz/tips/linux-multiple-ssh-key-based-authentication.html
