### Samba安装

安装samba应用 ： yum -y install samba samba-client 

启动Samba服务：systemctl start smb

重启Samba服务：systemctl restart smb

关闭防火墙：systemctl stop firewalld

禁止防火墙开机启动：systemctl disable firewalld

### 命令的常用方法

Linux系统用户
	添加系统用户：useradd ****
	删除系统用户：userdel -r *****	
	给新创建的用户设置密码：  passwd ****
	创建组：groupadd xzgroup
	创建组密码：gpasswd ****
	将用户添加到组：gpasswd -a [xzdoc] [xzgroup]
	查看用户：cat /etc/passwd
	查看用户组：cat /etc/group
	

### smbpasswd命令的常用方法：

pdbedit -L			查看用户

smbpasswd -a 	增加用户（要增加的用户必须是系统用户）

smbpasswd -d 	冻结用户，就是这个用户不能在登录了

smbpasswd -e 	恢复用户，解冻用户，让冻结的用户可以在使用

smbpasswd -n 	把用户的密码设置成空. 要在global中写入 null passwords -true

smbpasswd -x 	删除用户


创建文件夹：mkdir -p /mnt/xzdoc/doc/123
赋予权限：chmod -R 777 /mnt/xzdoc/doc/123


-rw------- (600)    只有拥有者有读写权限。
-rw-r--r-- (644)    只有拥有者有读写权限；而属组用户和其他用户只有读权限。
-rwx------ (700)    只有拥有者有读、写、执行权限。
-rwxr-xr-x (755)    拥有者有读、写、执行权限；而属组用户和其他用户只有读、执行权限。
-rwx--x--x (711)    拥有者有读、写、执行权限；而属组用户和其他用户只有执行权限。
-rw-rw-rw- (666)    所有用户都有文件读、写权限。
-rwxrwxrwx (777)    所有用户都有读、写、执行权限。



