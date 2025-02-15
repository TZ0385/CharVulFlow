**CharVulFlow_V1.0.1【补天 | 雷神 | 360众包】**

    ```
    _________ .__                ____   ____    .__  ___________.__                 
    \_   ___ \|  |__ _____ ______\   \ /   /_ __|  | \_   _____/|  |   ______  _  __
    /    \  \/|  |  \\__  \\_  __ \   Y   /  |  \  |  |    __)  |  |  /  _ \ \/ \/ /
    \     \___|   Y  \/ __ \|  | \/\     /|  |  /  |__|     \   |  |_(  <_> )     / 
     \______  /___|  (____  /__|    \___/ |____/|____/\___  /   |____/\____/ \/\_/  
            \/     \/     \/                              \/
    ```
<p align="center">
<a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/license-MIT-_red.svg"></a>
<a href="https://github.com/asaotomo/fofamap/issues"><img src="https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat"></a>
<a href="https://github.com/sqlmapproject/sqlmap/actions/workflows/tests.yml"><img src="https://img.shields.io/badge/python-3.7-blue.svg"></a>
</p>

### 项目目前需要修改的地方太多，能用但暂且不建议使用！！！这个月内会发布全新版本，敬请期待。
### 项目目前需要修改的地方太多，能用但暂且不建议使用！！！这个月内会发布全新版本，敬请期待。
### 项目目前需要修改的地方太多，能用但暂且不建议使用！！！这个月内会发布全新版本，敬请期待。
2023·10·10-2023·11·01

### 0x00、项目说明
1. 需求：满足公益漏洞大批量提交需要（尤其针对零权活动），减少人工时间成本；
2. 支持漏洞类型：GET类型请求，结果可直接回显浏览器（未授权访问、信息泄露、弱口令等);
3. 支持个性化制：自定义需要截图证明，建议提前与审核商量好提交。
4. 后续计划加入：权重检测模块，满足日常不参加活动公益漏洞提交。

### 0x01、配置文件

1. 在module.get_shoot修改适合你电脑的webdrive配置，参考：  
   - [Edge浏览器配置Selenium](https://blog.csdn.net/tk1023/article/details/109078613)    
   - Chrome浏览器配置Selenium需修改部分代码
   - 第17行代码需要修改为自己的电脑用户名，否则截图浏览器出现弹窗。


2. 在module.config填写需要的cookie以及apikey：
    - [补天公益提交入口](https://www.butian.net/Loo/submit/)；
    - [雷神公益提交入口](https://bug.bountyteam.com/index)；
    - [360众包提交入口](https://src.360.net/home)；
    - [站长之家API获取](https://my.chinaz.com/ChinazAPI/DataCenter/MyDataApi)；  
    - [滑块验证API获取](http://rrocr.com/)；
    ```
    [config]    # API：站长ICP|滑动验证
    chinaz = eaxxxxxxxxxxxxxxxxxxxxxxxxxxx43b 
    appkey = d2xxxxxxxxxxxxxxxxxxxxxxxxxxx52e
    
    [but]       # 补天
    cookie = wzws_sessionid=xxxxxx; PHPSESSID=xxxxxx; __btu__=xxxxxx; __btc__=xxxxxx; __btuc__=xxxxxx
    
    [thor]      # 雷神
    cookie = 25xxxxxx-d1b7-4277-a79d-xxxxxxxxxx35
   
   [bugcloud]   # 360众包
    cookie = sessionID=xxxxxx; Q_UDID=xxxxxx
    ```
4. 在url.txt填写能回显的所有url，选择注释main函数 **补天 is_but | 雷神 is_thor | 360众包 is_bugcloud** 选择平台运行。

### 0x02、使用效果
- jshERP-boot未授权访问为例：直接访问/jshERP-boot/user/getAllList;.ico即可获取所有用户账户密码。
![img_1.png](images%2Fimg_1.png)

- 程序运行截图

    ```
      0%|          | 0/3 [00:00<?, ?it/s]成功提交金华市xxxxx有限公司
     33%|███▎      | 1/3 [01:05<02:11, 65.51s/it]成功提交苏州xxxxx有限公司
     67%|██████▋   | 2/3 [02:08<01:04, 64.25s/it]成功提交广州xxxxx有限公司
    100%|██████████| 3/3 [03:23<00:00, 67.71s/it]
    ```
- 提交成功列表
    ![img_2.png](images%2Fimg_2.png)
    ![img_3.png](images%2Fimg_3.png)
- 漏洞详细
    ![img_4.png](images%2Fimg_4.png)

### 0x03、项目逻辑
- 运行流程结构
    ![img.png](images%2Fimg.png)
