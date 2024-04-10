# Quantum
![Quantum](https://socialify.git.ci/outmansec/Quantum/image?description=1&forks=1&issues=1&language=1&logo=https%3A%2F%2Fcdn.worldvectorlogo.com%2Flogos%2Fgo-8.svg&name=1&owner=1&pattern=Solid&pulls=1&stargazers=1&theme=Auto)

## 为什么选择它

- 跨平台支持,你可以在任何环境中使用它;
- 目前支持9种扫描模式、17种协议识别、2种信息探测、8种未授权检测、11种弱口令检测、内置EHole指纹识别规则;
- 支持基础协议识别和弱口令检测并发,提升检测效率;
- 引入了验证模式,结果更为准确;
- 引入了debug模式,调试更加方便;
- 可以使用prefix设置关键字根据内置模版生成弱口令;
- 支持以表格(xlsx)形式汇总结果;
  
## 快速使用

![](https://github.com/outmansec/Quantum/blob/master/images/demo.svg)

**命令参数**

```
Usage of ./Quantum:
  -c int
    	Set login concurrency nums e.g.: 4 (default 4)
  -debug
    	Show debug info
  -f string
    	set target file e.g.: ip.txt
  -log string
    	save log e.g.: text | json
  -m string
    	Set modes e.g.: alive
  -np
    	Not checking for alive.
  -o string
    	Save Output file e.g.: result.xlsx
  -p string
    	Set port e.g.: 22 | 22,80,3306 | 1-65535 (default "22,80,443,21,23,139,445,2121,2222,1433,1521,3306,3389,5432,6379,27017")
  -prefix string
    	Set password Prefixe.g.:admin
  -pwd string
    	Set password e.g.: 123456
  -pwdf string
    	Set password file e.g.: pass.txt
  -rate int
    	Set  Threads nums e.g.: 600 (default 600)
  -t string
    	Set target e.g.: 192.168.0.1 | 192.168.0.1,192.168.0.2 | 192.168.0.1-255 | 192.168.0.1-192.168.0.255 | 192.168.0.1/24
  -timeout int
    	Set  timeout (Millisecond) e.g.: 800 (default 3000)
  -user string
    	Set username e.g.:admin
  -userf string
    	Set username file e.g.: user.txt
  -v	Set verify login.
```

**支持9种扫描模式**

`alive`(存活检测)、`portscan`(端口扫描)、`servicescan`(基础协议识别)、`detect`(信息探测)、`unauthorized`(未授权检测)、`brute`(弱口令检测)、`ms17010`(ms17010检测)、`webfinger`(web指纹识别)、`all`(全部)

**支持17种协议识别**

`FTP`, `SSH`, `Telnet`, `NetBIOS`, `HTTP`, `HTTPS`, `SMB`, `MSSQL`, `Oracle`, `MySQL`, `RDP`, `PostgreSQL`, `Redis`, `MongoDB`,`Memcached`,`Zookeeper`,`Jdwp`

**支持2种信息探测**

| 序号  | 协议 | 信息 |
| :------:  | :------: | -------- |
|1|   t3   | 版本信息 |
|2|   iiop  | 协议探测 |

**支持8种未授权检测**

| 序号  | 协议 | 是否支持验证 | 验证方法 |
| :------: | :------: | :------: | -------- |
|1|   ftp    | ✅ | 目录信息 |
|2|     telnet  | ✅ | 登陆信息 |
|3|   smb  | ✅ | 目录信息 |
|4|   redis   | ✅ | info信息 |
|5|  mongodb  | ✅ | 版本信息 |
|6|  memcached  | ✅ | stats信息 |
|7|  zookeeper  | ✅ | envi信息 |
|8|  jdwp  | ✅ | 返回信息 |

**支持11种弱口令检测**

| 序号 | 协议 | 是否支持验证 | 验证方法 |
| :------: | :------: | :------: | -------- |
|1|    ftp    | ✅ | 目录信息 |
|2|    ssh    | ✅ | 执行命令 |
|3|    Telnet  | ✅ | 登陆信息 |
|4|    smb    | ✅ | 目录信息 |
|5|    mssql   | ✅ | 版本信息 |
|6|   oracle  | ✅ | 版本信息 |
|7|   mysql   | ✅ | 版本信息 |
|8|   rdp    | ❌ | 不支持 |
|9|   postgres | ✅ | 版本信息 |
|10|   redis   | ✅ | info信息 |
|11|  mongodb  | ✅ | 版本信息 |

**支持那些web指纹检测**

内置EHole规则




