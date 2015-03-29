# Gitbook 101

## Gitbook 是什么

网络发布的开源电子书，发布平台 www.gitbook.com

## Gitbook 的建立

* 注册（或用 Github 等账号登陆）后，在 Gitbook 首页的右上角点击 Create New Book 建立新书。记得 Copy 下来用于 push 的地址，比如本书的 push 地址是：“http://git.gitbook.com/ziyanziyan/codeeye.git”。 

* 在本地用 Markdown 编辑器按照 Markdown 语法编辑。


## 与 Github 连接推送

* 如果要用 Github 代码推送，就在建立时用 Github 账户登陆

* 新建的书在 Edit 的 Github Integration 中填入这本书在 Github 中的 repository 地址，并 Add a webhook

* Clone 那个 Github 的 repository 到本地

* 在本地的 Terminal 中进入本地 repository，使用代码 “$ cd repository_name”，使用 “$ git init” 初始文件夹

* 然后使用 “vi ./.git/config” 进入 config，按 “i” 进入 INSERT 模式，在[remote "origin"]的段落加入 url = gitbook 链接，然后按 esc 退出 INSERT 模式，输入 “:wq” 退出 config

* 完整地 config 信息如图：

  ![Config](images/config.png) 
	
* 第一次的推送代码是 “$ git push -u origin master”，之后就不用写 “-u” 了。

* 当提示需要输入用户名和密码时有一个需要注意的地方：输入密码并不在 Terminal 内显示任何变化，就像没输入一样，但实际上它在记录哦，所以认真敲对之后按回车就好了，它会继续验证。

## 增加 Disqus
* 在 https://disqus.com 上注册
* 注册后在右上角设置中选择 Add Disqus to your site，其 Choose your unique Disqus URL 中在 .disqus 之前的部分将成为你在 GutHub 的 book.json 中引用的shortname。
* 设置好后可通过 [你的shortname].disqus.com 进入这个版块
在 book.json 中添加
   
        {
            "plugins": ["disqus"],
            "pluginsConfig": {
                "disqus": {
                    "shortName": "[你的shortname]"
                }
            }  
        }

* 推送后即可在 Gitbook 中看见评论版。

## 在本地发布 PDF

鉴于从 Gitbook 网站下载的 PDF 中文字体过于奇葩，于是尝试使用 Node.js 本地发布。

* Node.js 是什么  
Node.js是一个基于Chrome JavaScript运行时建立的平台， 用于方便地搭建响应速度快、易于扩展的网络应用。  

* Gitbook 配置，见[链接](http://www.joyios.com/?p=164)
	* 可能遇到的问题（都不懂原理惹...）
		1. 是否需要 sudo
		2. 是否需要科学上网
		3. unlock 问题，见[链接](https://github.com/npm/npm/issues/4815)，我使用其中的  
	
	            sudo chown -R `whoami` ~/.npm
                sudo chown -R `whoami` /usr/local/lib/node_modules
     和  
     
            sudo chown -R `whoami` /usr/local
         
          解决了问题..
* 下一步就是调整格式，把 PDF 变好看啦。  
     
## 遇见并拍死了哪些 Bug

* Gitbook 推送失败 while 同时推送的 Github 成功。在 Gitbook 的 History 中看见红色的叹号，提示“Cannot read property 'text' of undefined”。经 Google 了解到是因为 SUMMARY.md 中 list 和 list 之间被我不小心多加了空行。

## 偷偷告诉你的 Tips

最快的学习方法是 Fork 一本完成的书，研究模仿各个文件的架构和写法，再写自己的。







