# 介绍
微内核进程管理、进程间通信IPC、回调Callback、CLI、Signal实现

# 特性
- 支持进程创建和资源管理
- 支持进程间通信
- 支持内核回调用户态接口
- 支持内核管理用户态注册的CLI命令
- 支持Signal

# 目录
```sh

├── aos.mk
├── Config.in
├── core_ipc                    #进程间通信IPC
│   ├── aos.mk
│   ├── Config.in
│   ├── include
│   │   ├── kipc_perf.h
│   │   ├── kipc_queue.h
│   │   └── kipc_utils.h
│   ├── ipc.c
│   ├── ipc_fifo.c
│   ├── ipc_msg.c
│   ├── ipc_perf.c
│   ├── ipc_queue.c
│   ├── ipc_str.c
│   ├── ipc_stream.c
│   └── ipc_uds.c
├── core_src                    #进程创建、回调Callback、CLI、Signal实现
│   ├── ash.c
│   ├── callback.c
│   ├── fsfd.c
│   ├── ipc.c
│   ├── res.c
│   ├── socketfd.c
│   ├── task_group.c
│   ├── ucli.c
│   ├── usignal.c
│   ├── uspace_init.c
│   └── utask.c
├── include
│   ├── callback.h
│   ├── dyn_syscall.h
│   ├── fsfd.h
│   ├── iomap.h
│   ├── ipc.h
│   ├── mk_default_config.h
│   ├── mksh.h
│   ├── res.h
│   ├── socketfd.h
│   ├── task_group.h
│   ├── ucli.h
│   └── utask.h
├── mksh                       #进程资源管理
│   ├── aos.mk
│   └── mksh.c
└── README.md

```
# 依赖
- ksyscall
- mksh
- core_ipc

# 使用
N/A

# 参考
N/A


# 介绍
用户态内存管理、线程管理、定时器、回调、CLI等

# 特性
- 支持用户态动态内存管理
- 支持用户态任务管理
- 支持用户态定时器管理
- 支持用户态执行回调函数
- 支持用户态执行CLI命令

# 目录
```sh

├── aos.mk
├── Config.in
├── include
├── README.md
└── src
    ├── callback_task.c     #用户态回调函数执行
    ├── cli_task.c          #用户态CLI命令执行
    ├── debug               #调试打印相关
    │   ├── debug_api.c
    │   ├── debug_print.c
    │   └── debug_test.c
    ├── res_task.c
    ├── uassert.c
    ├── umm                 #用户态动态内存管理
    │   ├── u_mm_blk.c
    │   ├── u_mm.c
    │   └── u_mm_debug.c
    ├── utask.c             #用户态线程管理
    └── utimer.c            #用户态定时器管理

```
# 依赖
- usyscall

# 使用
N/A

# 参考
N/A

