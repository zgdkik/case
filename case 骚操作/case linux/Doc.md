# Linux 操作笔记



## 基本信息

```
> 账号密码 
 -> root
 -> zzg19950824
 
> vm net 范围 
 -> 192.168.158.2
 -> CentOS 静态 ip : 192.168.158.20
```



## 常用命令  -  网络

```
> 查看 IP 信息 --- ifconfig
> 访问网络 --- telnet 
  -> 查看 telnet 服务 --- rpm -qa telnet-serverc
> 重启网络 --- service network restart
```



## 操作流程

```
> 编辑文档
 -> vi filename
 -> 按 i 进入编辑
 -> vm 中 shift + Esc 退出
 -> :wq 

> 联网 ： 
  -> vi /etc/sysconfig/network-scripts/ifcfg-ens33
  -> ip addr
  
> 安装 yum
  -> 查看 yum 版本 --- rpm –qa|grep yum
  
  
> 安装 JDK
  -> 检查是否已经安装 JDK --- yum list installed | grep java
  -> 查看 JDK 安装列表 --- yum search java | grep -i --color jdk 
  
>   
```





### 常见问题

##### yum doesn't have enough cached data to continue

```
1  >  将/etc/yum.repos.d/epel.repo中的mirrorlist改为baseurl
2  >   /etc/resolv.conf文件中增加nameserver 144.144.144.144

[root@ec-cache ~]# vi /etc/resolv.conf

# Generated by NetworkManager
nameserver 192.168.1.2
nameserver 144.144.144.144
```

