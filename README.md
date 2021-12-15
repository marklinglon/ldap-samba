# ldap-samba
```
1.ldap创建的普通用户登录jumpserver等都比较简单实现
2.ldap创建的普通用户和samba用户都不能登录samba用，必须使用smbpasswd -a username创建ldap用户，而且创建之前，samba系统上也必须有这个用户，useradd username
3.smbpasswd 给samba设置ldap管理员密码，否则samba启动不起来
4.smbpasswd添加的用户会自动同步到ldap，但是需要手动给用户创建NTpasswd和LMpassword
5.需要smbpasswd -U username，更新密码后，用户才能使用，否则netbios会报首次登录需要更新密码
```
