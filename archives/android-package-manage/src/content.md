# Android 包管理

- - -

## 管理什么包？

![](http://onhff7qaf.bkt.clouddn.com/android-package-2.png)

Note: Jar包、aar、Apk、so

- - -

### Jar

![](http://onhff7qaf.bkt.clouddn.com/android-package-6.png)

- - -

### aar

![](http://onhff7qaf.bkt.clouddn.com/android-package-4.png)

- - -

### Apk

![](http://onhff7qaf.bkt.clouddn.com/android-package-5.png)

- - -

## 包管理的发展历史
- Ant 时代
- Maven 时代
- Gradle 时代
Note: ant 静态包依赖, maven 动态包依赖, gradle 更加灵活的构建过程定义

- - -

#### Android 的整个打包流程
![打包流程图](http://onhff7qaf.bkt.clouddn.com/build-process_2x.png?imageView2/2/w/600/q/75|imageslim)

Note: 

- - -

#### Android 目录结构
![](http://onhff7qaf.bkt.clouddn.com/project-structure_2x.png?imageView2/2/w/500/q/75|imageslim)

- - -

## build.gradle 解读
-  project build.gradle
-  module build.gradle

- - -

#### project build.gradle
![](http://onhff7qaf.bkt.clouddn.com/android-package-7.png)
Note:  全局作用域，一般配置中心库及私服的位置 一些全局插件的声明

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

##  编译过程 gradle task

1. Preparation of dependecies
2. Merging resources and processing Manifest 
3. Compiling
4. Postprocessing
5. Packaging and publishing

