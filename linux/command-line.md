# Linux

- Linux  is Open Sorce Operating system that can be modified by you.

- Anyone can addn, remove code in linux.

- Linux is used for android mobiles as Operating system also

- More secure than Windwos

- More fast than Windows

- Provides all Haking tools For Free

## Ther are distribution for linux : 

- Debian (kali)

- Ubuntu

- Red Hat

- Fedora

- Centos ...

# Command Line

### After installing the system open treminal and update it by:

- `sudo apt update` 
- `sudo apt upgrade`
- apt is used to install new applications in linux

### update & upgrade

- `update` downloads the list of the newest software version.

- `upgrade` install the newer versions of the software on yor system.
```
sudo apt update

sudo apt upgrade
```

### sudo

- sudo means super user or (high privileges)

- (when you see (premission denised)) use :
```
sudo
```
### some command 

- To see the current user
```
whoami
```
- To see files on same directory or folder
```
ls
```
- To see the current folder 
```
pwd
```
- To move to folder 

```
cd
```
- To get back to previous folder

```
cd ..
```
- To read file called name.txt

```
cat name.txt
```
- then write then CTRL+X then Y 
```
nano name.txt
```

- To remove file called name.txt

```
rm name.txt
```
- To create new folder called tom

```
mkdir tom
```

- To remove the folder tom 

```
rm -r tom
rm -r /home/kali/name
```

- Ther are tow types of paths :

- absolute path starts with /
- Ex: /home/name/downloads/
- Relative path :
It is current path and you don't need to discribe the full path 

------------------------------

- copies files and folders.
```bash
cp file.txt backup.txt
cp file.txt /home/user/Documents/
```

--------------------------------

- `mv` moves files and folders from one place to another.

```bash
mv file.txt /home/user/Documents/
mv oldname.txt newname.txt
mv myfolder/ /home/user/Documents/
```

--------------------------------

### Defference between write and append
- To write is to add new content to file but deletes the old content
- To append is to add new content without deleting old content

```bash
echo "hello" > file.txt
echo "world" >> file.txt
cat file.txt
```
----------------------------

- To get informaton about network

```bash
ifconfig
```

![ifconfig output](images/ifconfig.png)
-------------------------------------

- To get information about memory space

```bash
free
```
![free output](images/free.png)
- To get information about hard disk

```bash
df -h
```
- To information about %CPU

```bash
ps aux
```

- To kill a process

```bash
kill PID
```

------------------------------------

- There are many ways to install applications in linux.

- First: use # `apt install <application>`
- Second: use # `snap install <application>`

- Third use # `dpkg -i <application.deb>`

![install application](images/install.png)

----------------------------------

- Permissions for files are (read write execute ).

- Execute => 1 =>
x
- Write =>
2 => W
- Read => 4 =>
r
- If you need read & write then 4+2 = 6

- To change the permissions for a file xyz.txt 
```bash
chmod 777 xyz.txt
```
- To add execute permission to a file xyz.txt 
```bash
chmod +x xyz.txt
```
