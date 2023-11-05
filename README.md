# Gatling
Gatling 是一款基于golang开发的综合漏洞扫描工具,目前支持存活检测、端口扫描、服务检测、弱口令检测.



## 命令参数

|  参数   |                             含义                             |
| :-----: | :----------------------------------------------------------: |
|    t    | 设置扫描目标格式如下:192.168.0.1;192.168.0.1,192.168.0.2;192.168.0.1-255;192.168.0.1-192.168.0.255;192.168.0.1/24; |
|    f    | 设置扫描列表格式如下:192.168.0.1;192.168.0.1,192.168.0.2;192.168.0.1-255;192.168.0.1-192.168.0.255;192.168.0.1/24; |
|    m    |     设置扫描模式目前支持alive;portscan;servicescan;brute     |
|    p    |     设置扫描端口不设置使用默认配置格式如下1-65535;22,23      |
|  user   |  设置弱口令检测用户名不设置使用默认配置如:admin;root,admin   |
|   pwd   |  设置弱口令检测密码不设置使用默认配置如:123456;123456,admin  |
|  userf  |                   设置弱口令检测用户名列表                   |
|  pwdf   |                      设置弱口令检测列表                      |
|  rate   |   设置IP并发数量默认为600;服务检测、弱口令为设置并发数/10    |
|    c    |              设置单IP弱口令检测并发数量默认为8;              |
| timeout |                         设置超时时间                         |
|    v    |                      验证弱口令检查结果                      |
| prefix  |     设置一个关键词根据内置模版生成更多口令如huawei,h3c等     |
|   np    |                          不检测存活                          |
|   bt    |           设置登陆最大连接时间,超过则不在检测目标            |

## 可以检测那些服务

| 序号 | 默认端口 | 默认协议 |
| :------: | :------: | :------: |
|1|    21    |   FTP    |
|2|    22    |   SSH    |
|3|    23    |  Telnet  |
|4|    80    |   http   |
|5|   139    | Netbios  |
|6|   443    |  Https   |
|7|   445    |   smb    |
|8|   1433   |  Mssql   |
|9|   1521   |  Oracle  |
|10|   3306   |  Mysql   |
|11|   3389   |   rdp    |
|12|   5432   | postgres |
|13|   6379   |  redis   |
|14|  27017   | mongodb  |

## 支持那些弱口令检测
| 序号 | 默认端口 | 默认协议 | 是否支持验证 | 验证方法 |
| :------: | :------: | :------: | :------: | -------- |
|1|    21    |   FTP    | 是 | 目录信息 |
|2|    22    |   SSH    | 是 | 执行命令 |
|3|    23    |  Telnet  | 是 | 登陆信息 |
|4|   445    |   smb    | 是 | 目录信息 |
|5|   1433   |  Mssql   | 是 | 版本信息 |
|6|   1521   |  Oracle  | 是 | 版本信息 |
|7|   3306   |  Mysql   | 是 | 版本信息 |
|8|   3389   |   rdp    | 否 | 不支持 |
|9|   5432   | postgres | 是 | 版本信息 |
|10|   6379   |  redis   | 是 | info信息 |
|11|  27017   | mongodb  | 是 | 版本信息 |

## 更新日志

**0.3.0**

1. 修复ssh登陆长等待导致爆破进度无法进行问题;

2. 修复telnet误报问题,支持登陆验证;
3. 修复ftp误报问题;
4. 优化单ip并发数;

**0.2.0**

1. 修复telnet登陆长等待导致爆破进度无法进行问题
