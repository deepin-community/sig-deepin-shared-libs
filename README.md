# deepin-shared-libs
  deepin-shared-libs旨在为各大编译玩家提供交流平台，大家可以在这里通过共创的形式分享自己在编译应用/库过程中积累的各类操作文档和可重复使用的二进制资源，主要为动态库和二进制可执行程序。这里是用来放置文档、二进制发行资源的仓库。

## 版本周期控制
  目前主要分为main和test两个分支，原则上主要处理main分支提交的issue

|main|test|
|-------|------|
|自贡献之时起一个月内没有issue反馈的库/应用|新贡献未经过验证的库/应用|


## 贡献方法

  目前贡献途径尚未完善，PR途径仅支持对文本、目录的创建、修改，如需贡献二进制资源请与我联系。


## 分发要求
  为了对各大开发者提供尽可能完善的便利性和降低权限错误带来的影响，请大家尽量将库打包为 **tar.xz格式的压缩包** 上传。
  这样其他开发者进行二次引用、分发时就不需要再单独区分include、lib目录，对于喜欢单独管理每个独立库的爱好而言是比较方便的。


### 目录&文件名规范
  仓库内的资源应当能够直接表示：动态库名称、动态库版本号、动态库编译日期、动态库维护人github用户名。除满足以上基本要求外，可根据个人需求添加其他名称标识

  示例：由szbt贡献的的Qt5.15.10动态库、支持OpenGL ES，自定标识版本为"231020~szbt"，则对应路径和文件分布应当为:


```
├── main
│   └── Qt
│       ├── 5.15.10
│       │   └── OpenGLES
│       │       └── 231020~szbt
│       │           ├── changelog.md
│       │           ├── config.summary
│       │           ├── info
│       │           ├── Release.md
│       │           └── tested.md
```



本仓库也提供了一个example目录示例，可以以此为参考

## 开源激励计划
  为鼓励更多人可以学习编译、交流经验，鼓励每位贡献者在资源压缩包内提供编译时所用到的参数、报错解决方案等，形式不限。

  同时我也很支持大家能够将本SIG的资源运用到其他发行版上，推进兼容性优化和适应开源发展需求，鼓励贡献者、参与者在非deepin的其他发行版上验证该库的兼容性。



