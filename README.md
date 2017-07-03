# yworkoffline

##说明

基于gulp任务流的模板和静态资源 打包工具

## 安装

安装npm install -g yworkoffline

采用的是全局安装,命令行调用。

## 基础配置

1.由于工具是基于yworkflow二次开发，所以需要xx.yconfig 文件 ；

    .yconfig文件具体配置见 https://github.com/yued-fe/Yworkflow

2.在项目中新建yworkoffline.config.json配置文件
    
    {
        "src":{
            "static":".cache/static",
            "views":".cache/views",
            "config":"src/offlineFile/config.json",
            "offlineConfig":"src/offlineFile/offline_config.json"
        },
        "build":{
            "static":"dist/static",
            "views":"dist/views"
        },
        "offline":{
            "static":"dist/offline/1/static",
            "views":"dist/offline/1/views",
            "config":"dist/offline/1",
            "offlineConfig":"dist/offline"
        },
        "buildPath":"dist",
        "zipPath":"dist/offline",
        "zipName":"1"
    }

## 使用方式

由于yworkoffline将核心构建任务完全配置化。可以理解成，通过上面的yworkoffline.config.json配置静态资源和views，以及打包文件的入口和出口。

不再强制约束文件夹格式，适用性更广。只需要保证保证框架机核心config配置，静态资源和模板自由度路径自由度更高。

### 发布

cd {项目目录} && yworkoffline --publish 


