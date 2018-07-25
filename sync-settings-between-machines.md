# 在机器之间同步 Intellij IDEA 配置

在配置同步之前，首先有几个外部依赖需要解决：1. 使用的同步服务，这里我推荐使用[Dropbox](https://db.tt/isyvu6ny) 2. 明确本地 Intellij IDEA 配置存储的路径

## 配置Intellij IDEA从同步文件夹读取配置
在之前[IDEA 各个目录作用](installation-directory-introduce.md) 中提到 config 目录：

> `config` 目录是 IntelliJ IDEA 个性化化配置目录，或者说是整个 IDE 设置目录。这个目录主要记录了：IDE 主要配置功能、自定义的代码模板、自定义的文件模板、自定义的快捷键、Project 的 tasks 记录等等个性化的设置。

在 `Help | Edit Custom Properties` 中开启自定义的属性

然后指定

    # custom IntelliJ IDEA properties
    idea.config.path=~/Dropbox/IntellijIdea2018/config/
    idea.log.path=/tmp/IntellijIdea/

修改 `idea.properties` 属性文件中的 `idea.config.path` 值

建议同步时只同步 conf 文件夹， system 中包含一些缓存会很大，这是我们本地的大小：

    212M	./config
    956M	./system
    1.2G	.
    

## 在新机器中使用相同的方法
导入配置文件夹