## 使用 ##
    ** main.exe **
    带参数的在命令行运行以获取带有steam mod信息的csv。
    例如：main.exe --appid=281990 --proxy_port=7890
    由于众所周知的原因，代理一定记得上
    ** 参数 **
    --appid:int,Steam AppID,比如群星是281990，你可以在游戏的创意工坊
    --concurrent:int,同时运行的协程数，越高越快，但是有概率被429，默认值16，群星3w个项目大约耗时20分钟
    --start:int,起始页码
    --end:int,结束页码,不填则是所有
    --timeout:int，请求超时时间（秒）
    --retries:int,单页最大重试次数
    --min_sleep:float,请求后最小随机休眠（秒
    --max_sleep:float,请求后最大随机休眠（秒）
    --proxy_port:type=int, 本地代理端口号，0表示不使用代理
    ** steam_cmd.exe **
    带参数的在命令行使用，需要csv相对其在<游戏ID>/目录下。
    获取在steamcmd使用的命令以批量下载
    例如 steam_cmd.exe 281990

    
