## 基于swoole的crontab服务

### 1.设计初衷
我们经常会遇到一些需要延迟或者定时处理的后台任务，很自然想到的是使用linux提供的crontab服务定时执行，但是有一些不太方便的地方：  
- 1.如果服务器比较多，需要在不同服务器上设置任务，不易管理  
- 2.没有很好的版本控制，历史记录不方便查询  
- 3.crontab只支持到分钟

### 2.特点
- 1. 提供简单的api和管理界面，方便任务管理
- 2. 支持多服务器管理，服务器配置简单灵活
- 3. 支持秒级定时任务
- 4. 支持任务的热部署，不用重启服务

