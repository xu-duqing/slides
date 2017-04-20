# Android 包管理

- - -

## 管理什么包？

![](http://onhff7qaf.bkt.clouddn.com/android-package-2.png)

Note: Jar包、aar、Apk、so、war

- - -

### Jar

![](http://onhff7qaf.bkt.clouddn.com/android-package-6.png)
Note: class集合

- - -

### aar

![](http://onhff7qaf.bkt.clouddn.com/android-package-4.png)
Note: class + 资源集合

- - -

### Apk

![](http://onhff7qaf.bkt.clouddn.com/android-package-9.png?imageView2/2/w/1000/q/75|imageslim)

Note: dex + 资源集合

- - -

## Java构建工具的发展历史
- Ant 时代
- Maven 时代
- Gradle 时代

Note: ant 静态包依赖,作为Java工程构建鼻祖。它确定了Java工程的基本结构。
(1) src存放文件。
(2) class存放编译后的文件。
(3) lib存放第三方JAR包。
 maven 动态包依赖,
 核心特点：依赖管理、仓库、约定优于配置
gradle 更加灵活的构建过程定义
任务：task 作为gradle的一等公民
任务之间可以依赖。
最终由任务链完成构建工作

接下来重点放在Gradle的构建过程

- - -

#### Android 目录结构
![](http://onhff7qaf.bkt.clouddn.com/project-structure_2x.png?imageView2/2/w/500/q/75|imageslim)

Note: 从Android的目录开始

- - -

## build.gradle 解读
-  project build.gradle
-  module build.gradle

Note: 重点解读gradle文件，

- - -

#### project build.gradle
![](http://onhff7qaf.bkt.clouddn.com/android-package-7.png)
Note:  全局作用域，一般配置中心库及私服的位置 一些全局插件，任务的声明

- - -

#### module build.gradle
![](http://onhff7qaf.bkt.clouddn.com/android-package-8.png)
Note:   - 模块作用域，用于定义编译类型
        - 编译依赖
        - 构建参数
        - 构建过程定制
        - 覆盖率统计
        - 分渠道包
        - 混淆定义
        - 静态代码检测

- - -

#### Android 的整个打包流程
![打包流程图](http://onhff7qaf.bkt.clouddn.com/build-process_2x.png?imageView2/2/w/600/q/75|imageslim)

Note: 

- - -

##  编译过程 gradle task

1. Preparation of dependecies
2. Merging resources and processing Manifest 
3. Compiling
4. Postprocessing
5. Packaging and publishing

Note: 
1. 准备依赖: 在这个阶段gradle检测module依赖的所有library是否ready。如果这个module依赖于另一个module，则另一个module也要被编译。
2. 合并资源处理Manifest
3. 编译: 在这个阶段处理编译器的注解，源码被编译成字节码
4. 后处理: 所有带 “transform”前缀的task都是这个阶段进行处理的  生成dex
5. 打包和发布： 这个阶段library生成.aar文件，application生成.apk文件

