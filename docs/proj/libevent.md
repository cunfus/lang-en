# libevent 事件驱动网络库

选取了 [`1.4.3-stable`][1] 版本，看一下主要文件 `ll *.c | awk '{print $NF}'`，再精简下，只分析以下文件，顺带用 `cloc` 看下行数，合计 1529 行。

```bash
buffer.c     300  基础缓冲区操作
epoll.c      257  linux 后端的事件处理机制
evbuffer.c   259  事件驱动中的缓冲区管理
event.c      713  主逻辑
```

## 基本结构



## 主逻辑








---

[1]: [https://github.com/libevent/libevent/releases/tag/release-1.4.3-stable]