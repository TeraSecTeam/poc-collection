# poc-collection

poc-collection 是对 github 上公开的 PoC 进行收集的一个项目。

> Author : Ali0th
> 
> Team : TeraSecTeam

## 说明

poc-collection 是对 github 上公开的 PoC 进行收集的一个项目，目前主要收集  pocsuite 格式的python类 PoC，后续再优化其它格式。

## poc 脚本库下载

因为采集脚本的数据库较大，因此放在 sqlite3 文件中。

## sqlite3 库文件操作

```bash
# 进入 sqlite3 数据库
sqlite3 data.db

# 查看表格
.tables

# 统计所有 PoC
SELECT COUNT(*) FROM pocs;

# 获取第一条 PoC
SELECT * FROM pocs LIMIT 1;

# 统计所有带 thinkphp 的 PoC
SELECT COUNT(*) FROM pocs WHERE fileHTML LIKE '%thinkphp%';

# 选择第一条 PoC
SELECT * FROM pocs WHERE fileHTML LIKE '%thinkphp%' LIMIT 1;

# 退出
.q
```