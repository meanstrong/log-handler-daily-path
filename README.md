# log-handler-daily-path - 一个每日切换日志路径模块

## About
这是一个日志路径每日轮转模块，按照指定方式每日切换日志输出路径。  

## Requirements
- Python3

## Install
通过pip命令安装：
```shell
pip install log-handler-daily-path
```

## Usage
```python
import logging

from daily_rotating_path_hander import DailyRotatingPathHander


logging.basicConfig(level=logging.DEBUG)
log_handler = DailyRotatingPathHander(base_path="/var/log", filename="app.log", backup_days=30)
logging.getLogger().addHandler(log_handler)

logger = logging.getLogger("Logger")
logger.info("xxx")
```


## Author
- <a href="mailto:pmq2008@gmail.com">Rocky Peng</a>
