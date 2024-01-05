# Quantum
![Quantum](https://socialify.git.ci/outmansec/Quantum/image?description=1&forks=1&issues=1&language=1&logo=https%3A%2F%2Fcdn.worldvectorlogo.com%2Flogos%2Fgo-8.svg&name=1&owner=1&pattern=Solid&pulls=1&stargazers=1&theme=Auto)

## 免责声明

该工具仅用于安全自查.

由于传播、利用此工具所提供的信息而造成的任何直接或者间接的后果及损失，均由使用者本人负责，作者不为此承担任何责任.

本人拥有对此工具的修改和解释权。未经网络安全部门及相关部门允许，不得善自使用本工具进行任何攻击活动，不得以任何方式将其用于商业目的.  

## 为什么选择它

- 目前支持存活检测、端口扫描、基础协议识别、弱口令检测、ms17010检测、web指纹识别;
- 支持登陆并发,提升扫描速度;
- 支持基础协议识别,提高检测效率;
- 支持登录验证,结果更为准确;
- 引入了debug模式,调试更加方便;
- 支持以表格形式汇总结果;
  
## 快速使用
[](https://github.com/outmansec/Quantum/assets/61048948/7c380e4a-c751-4abe-9b82-33580dd0b094)

**命令参数**

|  参数   |                             含义                             |
| :-----: | :----------------------------------------------------------: |
|    t    | 设置扫描目标格式如下:192.168.0.1;192.168.0.1,192.168.0.2;192.168.0.1-255;192.168.0.1-192.168.0.255;192.168.0.1/24; |
|    f    | 如ip.txt,文本每行一个,格式参照-t |
|    m    |     设置扫描模式目前支持alive、portscan、servicescan、brute、ms17010、webfinger、all    |
|    p    |     设置扫描端口;不设置使用默认配置格式如下1-65535;22,23      |
|  user   |  设置弱口令检测用户名;不设置使用默认配置如:admin、root,admin   |
|   pwd   |  设置弱口令检测密码;不设置使用默认配置如:123456、123456,admin  |
|  userf  |                    设置弱口令检测用户名列表如user.txt每行一个                   |
|  pwdf   |                    设置弱口令检测列表如pwd.txt每行一个                      |
|  rate   |   设置IP并发数量默认为600;服务检测、弱口令检测模块为设置并发数/10    |
|    c    |              设置弱口令检测单IP并发数量默认为4;              |
| timeout |                         设置超时时间默认为3000                         |
|    v    |                      验证检测结果                      |
| prefix  |     设置一个关键词根据内置模版生成更多口令如huawei,h3c等     |
|   np    |                          不检测存活                          |
|   o    |           保存扫描结果默保存格式为xlsx           |
|   debug    |           显示调试信息           |
|   log    |           保存日志如:-log text,支持text和json格式   |

**支持那些协议识别**

- ftp
- ssh
- telnet
- netbios
- http
- https
- smb
- mssql
- oracle
- mysql
- rdp
- postgres
- redis
- mongodb
  
**支持那些未授权检测**

| 序号  | 默认协议 | 是否支持验证 | 验证方法 |
| :------: | :------: | :------: | -------- |
|1|   FTP    | 是 | 目录信息 |
|2|     Telnet  | 是 | 登陆信息 |
|3|   smb  | 是 | 目录信息 |
|4|   redis   | 是 | info信息 |
|5|  mongodb  | 是 | 版本信息 |

**支持那些弱口令检测**

| 序号 | 默认协议 | 是否支持验证 | 验证方法 |
| :------: | :------: | :------: | -------- |
|1|    FTP    | 是 | 目录信息 |
|2|    SSH    | 是 | 执行命令 |
|3|    Telnet  | 是 | 登陆信息 |
|4|    smb    | 是 | 目录信息 |
|5|    Mssql   | 是 | 版本信息 |
|6|   Oracle  | 是 | 版本信息 |
|7|   Mysql   | 是 | 版本信息 |
|8|   rdp    | 否 | 不支持 |
|9|   postgres | 是 | 版本信息 |
|10|   redis   | 是 | info信息 |
|11|  mongodb  | 是 | 版本信息 |

**支持那些web指纹检测**

内置EHole规则




