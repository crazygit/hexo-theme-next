## hexo博客主题


根据自身需求修改[hexo-theme-next](https://github.com/iissnan/hexo-theme-next)主题，方便后期的维护及更新。


### 修改历史

* 2017-12-21 基于`v5.1.3`做定制
* 2018-01-20 更新到`v5.1.4`
* 2018-04-11 更新到`v6.1.0`


### Todo List

- [x] [配置第三方服务](http://theme-next.iissnan.com/third-party-services.html)
- [x] [内置标签](http://theme-next.iissnan.com/tag-plugins.html)
- [x] [进阶设定](http://theme-next.iissnan.com/advanced-settings.html)
- [x] [常见问题](http://theme-next.iissnan.com/faqs.html)


### 主题更新方法

下面以更新到版本`v5.1.4`为例

添加原主题仓库

    $ git remote add upstream https://github.com/theme-next/hexo-theme-next.git

更新代码

    $ git fetch upstream

合并要更新到版本的代码

    $ git merge v5.1.4 --allow-unrelated-histories

根据实际情况解决冲突。

冲突太多时，如果无法解决，可以直接覆盖本地的代码

    $ git merge -X theirs --allow-unrelated-histories --no-commit v5.1.4

然后根据需要修改`._config.yml`即可。

`README.md`文件的由于用来记录自己的更新历史，原仓库的`README.md`被放到了`README.offical.md`, 所以该文件不用解决冲突，只需要更新`README.offical.md`

    $ git reset README.md
    $ git checkout README.md
    $ git show v5.1.4:README.md > README.offical.md
