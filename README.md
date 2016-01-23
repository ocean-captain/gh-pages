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

