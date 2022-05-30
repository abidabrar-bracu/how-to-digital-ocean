First, login as root using `ssh root@IP`

```bash
adduser abid
sudo adduser abid
```
When asks for password, put `123456`, skip the rest (e.g. Full Name) by pressing `ENTER`
```
usermod -aG sudo abid
visudo
```

add the following line under `root    ALL=(ALL:ALL) ALL`
```
abid  ALL=(ALL:ALL) ALL
```

Press `CNTRL+O`, then `ENTER`, then `CNTRL+X`, then `ENTER`.

```
su abid
mkdir -p /home/abid/.ssh
chown -R abid:abid ~/.ssh
exit
cp ~/.ssh/authorized_keys /home/abid/.ssh
chown -R abid:abid /home/abid/.ssh
su abid
chmod -R go= ~/.ssh
```
