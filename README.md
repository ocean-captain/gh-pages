# gh-pages 页面

###How Creat Project Page
参考链接：[Creating Project Pages manually](https://help.github.com/articles/creating-project-pages-manually/)
- 首先，我们在github上创建一个项目仓库。
- 然后，将这么项目仓库克隆到本地。 

```command
git clone github.com/user/repository.git
```
- 接着，创建gh-pages分支。(分支名字必须是这个名字)

```command
cd repository  
git checkout --orphan gh-pages  
git rm -rf . 
#这个移除命令是移除master分支或者其他分支的内容，保证第一次创建的时候，仓库是干净的。
```
- 然后，添加内容到该分支。

```command 
echo "My Page" > index.html
```
- 最后，add,commit,push。  
``` command 
git add index.html
git commit -a -m "First pages commit"
git push origin gh-pages
```

## TODO 

- [ ] 怎么通过jekyll创建静态网站页面。

## DONE 
- [x] 怎么创建Project-Pages

## DOING
记录怎么使用jekyll创建静态网站页面

`参考链接：` [Using Jekyll with Pages](https://help.github.com/articles/using-jekyll-with-pages/#troubleshooting)
`参考链接：` [使用 GitHub, Jekyll 打造自己的独立博客](http://www.tuicool.com/articles/BVVBvu)

**貌似官网上说不管是uer pages 还是project pages页面发布后，github会处理jekyll语法的，不需要在本地安装jekyll。只是为了能在发布之前预览和调试页面，最好还是安装比较好。**

- 更新ruby。最低得2.0.0`sudo apt-get install ruby2.0` (这时默认的还是原先的ruby版本，需要手动更改这个指向[参考链接](http://group.cnblogs.com/topic/71243.html))

- 推荐使用rvm安装ruby。所以先安装rvm。
> curl -L get.rvm.io | bash -s stable --ruby

- 在安装rvm时，可能会报这样的错：public key not found（无法检查签名：找不到公钥），这时你的终端找到这句话：try downloading the signatures:

    gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3

然后执行gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3，然后再执行curl -L get.rvm.io | bash -s stable --ruby，安装完后会有这样的提示 * To start using RVM you need to run `source /home/shaozhenxing/.rvm/scripts/rvm` 执行它。然后ruby -v,gem -v 查看是否成功。[安装rvm出错处理方法](http://blog.csdn.net/caspiansea/article/details/47802331)


> \curl -L https://get.rvm.io | bash -s stable 
[参考链接](http://my.oschina.net/kelby/blog/193035)

- 安装rvm

> rvm requirements

- 安装rubyGem

- 安装bundler`gem install bundler`
- 安装jekyll `$ gem install jekyll`
