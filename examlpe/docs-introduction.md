# 文档介绍
  本文档用于介绍examlpe中各描述文件的作用，文件中包含注释内容，在实际使用模板时请删除所有注释.本文档并不包含所有字段的介绍，详情可到example中查阅具体文件示例.


## info(required)
  此文件用于记录本库/应用的基本信息

```
{
    "name": "DTK",	#库/应用名称
    "type": "library",	#库/应用类型
    "DSL-API	": ["none"],	#deepin-shared-libs API版本，预留待定
    "complier": "Clang13.0.1",	#编译本库/应用所使用的编译器及其版本
    "base": "UOS V20 1060",	#编译本库/应用所使用的系统版本/环境
    "maintainer": "ziggy",	#维护者标识
    "version": "5.6.17~szbt"	#本库/应用版本号，建议格式为"version~维护者自定义版本"
}
{
    "support-build-systems": [
        "shirodeb-recipes"
    ],
}
```

|目前支持的type类型|解释|
|-------|--------|
|library|动态库/runtime|
|application|应用|
|devel|开发库,include头文件等|


## tested.md(required)
  该文件用于记录本库/应用在不同系统环境上的兼容程度，原则上所有人在经过测试后均可以在此文本中写入你测试完好的系统环境信息。


## deps(required)
  该文件用于记录本库/应用所依赖的其他库，主要包括以下类型:

```
## deepin-shared-libs #来自"deepin-shared-libs"SIG组内的共享库，(必须)设置版本关系，(可选)标注具体库的维护者

## built-in #在本库提供的Release包中集成了不属于该源码构建的第三方库，(建议)标注该库的版本

## deepin20.9 #编译本库的系统环境中所依赖的运行库，(可选)标注该依赖的版本，包名必须与仓库源中的包名保持一致
```
 **注:每次更新依赖内容后需要更新顶部日期**

## Release.md(required)
  该文件用于记录本库/应用所衍生出的binary分发包，需要与"Release"栏目中发布的Tag名保持一致
  Tag命名格式:"version+维护者标识版本号(库/应用名称)"

  目前支持的分发格式:

1. deb等支持包管理工具的软件包格式
2. tar.xz归档压缩文件，命名格式为libxxx-version_arch(架构).tar.xz

  建议采用支持包管理工具的软件包格式以辅助记录依赖情况




## changelog.md(optional)
  该文件用于记录库/应用的变更记录，日期较新的内容相对置顶。格式如下:
```
# year.month.day
changed logs
```
  "changed logs"内根据实际需求填写变更记录，若该项目暂无更新计划或已确定不再维护，则不需要changelog.



## libs.list(optional)
  该文件用于记录本库中具体所包含的模块，一般只有多库多包合一的模式需要用到，比如single包模式的Qt5Core、Qt5Gui、KDE Framwork等.



## envs.md(optional)
  该文件用于提供该库/应用常用的环境变量设置
