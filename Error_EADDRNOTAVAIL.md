# npm运行报错Error: listen EADDRNOTAVAIL

今天在使用npm run dev 运行vue2.0项目的时候遇到了一个错误：

```
Error: listen EADDRNOTAVAIL 192.168.199.123:8081
```
![1.png](https://upload-images.jianshu.io/upload_images/65990-039f524283e707b2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

导致项目运行不起来，看字面意思大概是IP出了问题。
于是我检查了网络适配器=》internet 协议版本4（tcp/IPv4）属性，发现网络设置的是自动获得ip地址。

![2.png](https://upload-images.jianshu.io/upload_images/65990-1c5b204e230173a9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

由于路由器是随机分配ip地址的，自动获取的ip地址和项目配置文件里面手动设置的 host 不一致，那么监听一个不存在的ip地址，自然会报错：Error: listen EADDRNOTAVAIL。 
解决方法：
1. win + r 输入 cmd 进入命令行后，输入ipconfig/all 查询当前IPv4地址、默认网关和DNS服务器地址，然后设置固定的IP设置。 

![4.png](https://upload-images.jianshu.io/upload_images/65990-f6601cb76ec0b8f6.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

2. 最后在项目的配置文件中重新设置host 为IPv4的地址即可正常运行。 
然后找到config文件夹下的index.js文件，打开后，将host的值改为我上一步所得到的ipv4即可

![5.png](https://upload-images.jianshu.io/upload_images/65990-07263750a2924934.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
