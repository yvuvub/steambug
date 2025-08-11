## 使用说明

### main.exe

用于抓取 Steam 创意工坊 Mod 信息并保存为 CSV 文件。

#### 基本用法

main.exe --appid=281990 --proxy_port=7890
⚠️ 由于众所周知的原因，建议使用代理（--proxy_port 参数）。

参数列表
参数	类型	默认值	说明
--appid	int	无	Steam AppID，例如群星（Stellaris）是 281990，可在游戏创意工坊页面 URL 中找到
--concurrent	int	16	并发协程数，越高速度越快，但有概率触发 429 Too Many Requests 错误
--start	int	1	起始页码
--end	int	1000	结束页码，不填则抓取到最后一页
--timeout	int	20	单个请求的超时时间（秒）
--retries	int	3	单页最大重试次数
--min_sleep	float	0.5	每次请求后的最小随机休眠（秒）
--max_sleep	float	1.5	每次请求后的最大随机休眠（秒）
--proxy_port	int	0	本地代理端口号，0 表示不使用代理

steam_cmd.exe
用于根据生成的 CSV 文件，批量生成 SteamCMD 下载 Mod 的命令脚本。

基本用法
steam_cmd.exe 281990
使用说明
确保 <游戏ID>_steam_workshop_items.csv 文件位于 <游戏ID>/ 目录下
例如：

281990/281990_steam_workshop_items.csv
运行 steam_cmd.exe <appid> 会生成一个 steamcmd 可直接运行的下载脚本。

用 SteamCMD 运行该脚本即可批量下载创意工坊 Mod。
