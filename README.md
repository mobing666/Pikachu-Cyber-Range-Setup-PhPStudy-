# Pikachu Cyber Range Setup (PhPStudy)
使用PhPStudy搭建Pikachu靶场环境

PhPStudy下载地址: https://www.xp.cn

Pikachu靶场下载地址：https://github.com/zhuifengshaonianhanlu/pikachu  


## 1. PhPStudy安装

![image](https://github.com/mobing666/Pikachu-Cyber-Range-Setup-PhPStudy-/assets/32005209/b88063ea-6084-4511-b628-004f295c6758)

这里下载的是PhPStudy v8.1版本，安装的时候我选择自定义安装，然后放到想要的路径。

![image](https://github.com/mobing666/Pikachu-Cyber-Range-Setup-PhPStudy-/assets/32005209/9245aaaa-ff4f-483c-bc05-3fa51ccdc213)
![image](https://github.com/mobing666/Pikachu-Cyber-Range-Setup-PhPStudy-/assets/32005209/c1e8a773-1095-4ef9-a453-015bed04f775)

安装好后就启动Apache和MySQL，然后测试在浏览器访问localhost或127.0.0.1看看PhPStudy有没有问题。
![image](https://github.com/mobing666/Pikachu-Cyber-Range-Setup-PhPStudy-/assets/32005209/480373a9-2138-4b49-b8bb-d18961f0f297)
![image](https://github.com/mobing666/Pikachu-Cyber-Range-Setup-PhPStudy-/assets/32005209/a07b157d-5ce5-472f-833d-f17abfab122b)

浏览器显示站点创建成功，代表PhPStudy服务可以正常运行   


## 2. Pikachu靶场搭建

服务器环境PhPStudy能使用后，我们接下来就下载Pikachu靶场然后把文件放到PhPStudy的WWW目录里C:\phpstudy_pro\WWW
![image](https://github.com/mobing666/Pikachu-Cyber-Range-Setup-PhPStudy-/assets/32005209/aaf59cb7-eb28-43dc-adea-8cb6f98bd614)

接下来就是网页访问pikachu靶场，看看是否能成功
![image](https://github.com/mobing666/Pikachu-Cyber-Range-Setup-PhPStudy-/assets/32005209/7b79e94c-f986-4d8e-a4aa-c4431c427f79)

报错内容

Warning: mysqli_connect(): (HY000/1045): Access denied for user 'root'@'localhost' (using password: NO) in C:\phpstudy_pro\WWW\pikachu-master\index.php on line 14

浏览器可以访问到，不过靶场遇到报错，解决方案就是到C:\phpstudy_pro\WWW\pikachu-master\inc目录下的config.inc.php使用文本编辑器把define('DBPW', '');这一行的密码输入，然后浏览器重新访问
![image](https://github.com/mobing666/Pikachu-Cyber-Range-Setup-PhPStudy-/assets/32005209/fe6d7651-7757-4c1a-8ec0-eba74f5df149)
![image](https://github.com/mobing666/Pikachu-Cyber-Range-Setup-PhPStudy-/assets/32005209/a10d597a-5ba9-486f-ae5e-2b810887ff90)

![image](https://github.com/mobing666/Pikachu-Cyber-Range-Setup-PhPStudy-/assets/32005209/4887672e-c5ee-4748-9484-0b548b1ae9d7)

报错内容

Warning: mysqli_connect(): (HY000/1049): Unknown database 'pikachu' in C:\phpstudy_pro\WWW\pikachu-master\index.php on line 14

出现了新的报错，解决方案只需要访问localhost/pikachu-master/install.php，然后点击安装按钮就可以了
![image](https://github.com/mobing666/Pikachu-Cyber-Range-Setup-PhPStudy-/assets/32005209/464ce4a5-ddce-4e0b-bb26-867d37a06cab)
![image](https://github.com/mobing666/Pikachu-Cyber-Range-Setup-PhPStudy-/assets/32005209/e444e0ce-35d4-4bb9-bf61-845c6b44528b)
![image](https://github.com/mobing666/Pikachu-Cyber-Range-Setup-PhPStudy-/assets/32005209/e7a32dcb-6b94-476e-9be6-ea4727258e28)
![image](https://github.com/mobing666/Pikachu-Cyber-Range-Setup-PhPStudy-/assets/32005209/b9e18191-0f58-4f34-ac56-efdc32462d2e)

Pikachu靶场可以正常运行，接下来我们就更改域名解析吧
![image](https://github.com/mobing666/Pikachu-Cyber-Range-Setup-PhPStudy-/assets/32005209/6fa562fd-98ff-43f1-92f2-5021ca33d872)
![image](https://github.com/mobing666/Pikachu-Cyber-Range-Setup-PhPStudy-/assets/32005209/884ba2e4-47ee-4f51-8e37-5e0c6e2012ae)

点击确认后，Apache服务会重启，然后访问pikachu.com就可以跳转到靶场那里
![image](https://github.com/mobing666/Pikachu-Cyber-Range-Setup-PhPStudy-/assets/32005209/7f4f3f0e-4b01-45e8-ba83-069f114fbbe4)

