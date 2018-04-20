# 理想之光app卡尔马克思杯 自动答题
直接发送请求进行答题 不设置延时大概需要4s完成  
只需要修改配置文件添加必要信息 直接运行main.py 扫描二维码即可

# 注意
本来想着尽量不要作弊 发现大家都已经做完这次考试 就把源码的正式考试功能又改了回来

# 运行环境
#### Python版本
>Python 3.6.4
#### HTTP 请求库
>requests  安装方法
```
pip install requests
```

# 使用方法
### 修改input.ini
- init
   * wait_time 延时 单位s  
   * type 0训练 1正式  
- user
   * username 姓名  
   * school 学校  
   * id 学号  
   * institute 学院  
   * calss 班级  
### 运行
```
python main.py
```
成功后扫描同目录下二维码

# 可能的报错
配置文件有错

# 可能的BUG
有个什么心连心的题啊 他答案是D我也选的D 还是说我错结果就99了 看人品

# 感想
题目是从服务器发至本地 每做一题都发一条请求到服务器上 进行存储判分   
但是他居然把答案和题目一同发到了本地 (怀疑程序员故意的 方便自己作弊啊   
那我就抓包 获得这个数据 得到考卷id 题目id 正确答案序号 直接提交   
本来写的很复杂 想着 模拟登陆 获取cookie 模拟手机请求 添加cookie登陆信息 还要防着被封 再本地题库找答案   
然而后来发现居然不需要登陆 直接submit-answer就完事了 甚至你连浏览器都不需要伪装   
意思就是只要获得了考卷id和题目id 任何人随便怎么样都能做你的这份考卷   
删了之前写了2小时的代码(还没有成功模拟出来   
然后摸了30分钟把这个新的代码写完了   
又短又简单 特别基础   
途中还发现我选了D答案也是D结果还是99分的情况   
   
主要是写Java的 py代码没写过几行 写的很垃圾   
(语言表达能力垃圾 还不肯用标点符号鶸   

# 感想2
很多人不抓包 就改了一个简单版本  
之前想着对做过的人不公平 就悄悄让正式竞赛交不上去 实际好像都做了
