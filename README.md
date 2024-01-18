# Quantum
![Quantum](https://socialify.git.ci/outmansec/Quantum/image?description=1&forks=1&issues=1&language=1&logo=https%3A%2F%2Fcdn.worldvectorlogo.com%2Flogos%2Fgo-8.svg&name=1&owner=1&pattern=Solid&pulls=1&stargazers=1&theme=Auto)

## 免责声明

该工具仅用于安全自查.

由于传播、利用此工具所提供的信息而造成的任何直接或者间接的后果及损失，均由使用者本人负责，作者不为此承担任何责任.

本人拥有对此工具的修改和解释权。未经网络安全部门及相关部门允许，不得善自使用本工具进行任何攻击活动，不得以任何方式将其用于商业目的.  

## 为什么选择它

- 跨平台支持,你可以在任何环境中使用它;
- 目前支持存活检测、端口扫描、基础协议识别、弱口令检测、ms17010检测、web指纹识别;
- 支持登陆并发,提升扫描速度;
- 支持基础协议识别,提高检测效率;
- 支持登录验证,结果更为准确;
- 引入了debug模式,调试更加方便;
- 可以使用prefix设置关键字根据内置模版生成弱口令;
- 支持以表格形式汇总结果;
  
## 快速使用
![](https://github.com/outmansec/Quantum/assets/61048948/2b6a6506-c112-4aea-becf-e4504edfa8cf)

![](https://github.com/outmansec/Quantum/assets/61048948/eb07aabe-087d-4908-b0f3-602176156e6f)



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

**支持14种协议识别**

`FTP`, `SSH`, `Telnet`, `NetBIOS`, `HTTP`, `HTTPS`, `SMB`, `MSSQL`, `Oracle`, `MySQL`, `RDP`, `PostgreSQL`, `Redis`, `MongoDB`
  
**支持5种未授权检测**

| 序号  | 协议 | 是否支持验证 | 验证方法 |
| :------: | :------: | :------: | -------- |
|1|   FTP    | ✅ | 目录信息 |
|2|     Telnet  | ✅ | 登陆信息 |
|3|   smb  | ✅ | 目录信息 |
|4|   redis   | ✅ | info信息 |
|5|  mongodb  | ✅ | 版本信息 |

**支持11种弱口令检测**

| 序号 | 协议 | 是否支持验证 | 验证方法 |
| :------: | :------: | :------: | -------- |
|1|    FTP    | ✅ | 目录信息 |
|2|    SSH    | ✅ | 执行命令 |
|3|    Telnet  | ✅ | 登陆信息 |
|4|    smb    | ✅ | 目录信息 |
|5|    Mssql   | ✅ | 版本信息 |
|6|   Oracle  | ✅ | 版本信息 |
|7|   Mysql   | ✅ | 版本信息 |
|8|   rdp    | ❌ | 不支持 |
|9|   postgres | ✅ | 版本信息 |
|10|   redis   | ✅ | info信息 |
|11|  mongodb  | ✅ | 版本信息 |

**支持那些web指纹检测**

内置EHole规则




