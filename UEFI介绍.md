# UEFI介绍

[https://blog.csdn.net/weixin_45384176/article/details/100094898](https://blog.csdn.net/weixin_45384176/article/details/100094898)

[https://blog.csdn.net/xiaopangzi313/article/details/108014343](https://blog.csdn.net/xiaopangzi313/article/details/108014343)

### 使用EDK2

* 模块

元数据inf和源文件efi组成

* 包

一组模块和dsc dec文件组成的集合, inf文件相当于Makefile

### UEFI驱动模块类型

- 标准应用程序工程模块

- shell应用程序工程模块

- main应用程序工程模块

- UEFI驱动模块，符合uefi驱动模块的驱动，仅在BS阶段有效

- 库模块，作为静态库被其他模块调用

- DXE驱动模块，DXE阶段运行的驱动，不符合UEFI驱动模型

### UEFI驱动模块

- UEFI驱动模块

- DXE驱动模块

