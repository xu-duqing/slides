## Android Things Boot

- - -

### 什么是开源硬件？

Note: 开源软件好理解， 就是软件可以自由使用、拷贝研究。但是开源硬件指的是什么？自由使用？不要钱吗？其实这是很早之前我对开源的误解。其实开源是自由而不是免费。开源硬件指的是硬件的电路的设计、材料、布局是公开的。可以自用使用，拷贝的。当然是在符合对应许可证的情况下。

- - -

### 什么是 iot ？

Note: 其实就是互联网的扩展，终端从计算机到各种硬件设备。

- - -

### Android Things

![](https://img.makerdiary.co/20161216/AndroidThings.png)

Note: Google 推出的物联网操作系统,只要你会写App就可以做硬件

- - -

###  Android Things 架构

![](https://img.makerdiary.co/20161216/platform-architecture.png)

- - -

![](http://images.cnblogs.com/cnblogs_com/skynet/WindowsLiveWriter/Androidandroid_1C63/Android_system_architecture_thumb.jpg)

- - -

### 开始前的准备

## 树莓派 3 + SD卡 + 外设


- - -

### 第一步
# 烧卡

- - -

查看磁盘   
```
diskutil list
```

卸载磁盘   
```
diskutil unmountDisk /dev/disk2
```

写镜像    
```
sudo dd bs=1m if=/Users/Guang/Downloads/iot_rpi3.img of=/dev/disk2 conv=sync
```


- - -

### 第二步 
# 建立连接

[如何和Android Things建立连接](http://www.jianshu.com/p/905d58645fe3)

- - -

### 第三步 
# 开始你的表演

- - -



