# 为什么集

* 编程思维的优劣  
在尝试各种平台软件的时候会遇到各种 bug，使用 Google 几乎是找人手把手解决之外最好的方式。但在寻求答案的过程中发现，无数程序员写的东西都因为太有**编程思维**而看让人不懂惹。  
	* Mac 的目录是怎么回事（比对 Windows 的文件夹）？
	> Finder左栏的默认列表示意了一个非常清晰的内容组织结构，按照文件的位置（Dropbox、桌面）、类型（文稿、音乐、图片）、作用（下载、共享）、频度（我的所有文件）进行了划分，Windows中也有类似的结构，采用收藏夹和库的方式来组织文件。Finder中还增加了一个标记功能，通过颜色和自定义的标签对文档进行归类。  
Finder的文件划分结构下，**如果你还钟情于传统的文件夹管理方式，可以在「文稿」一级目录下再进行划分，目录结构保持两层就足够了，再增加实际应用的帮助不大，只会自寻烦恼。**  
传统的按文件的创建时间、名称排序之外，按应用程序、种类（文件后缀名）分组在某些场景中能更清晰的展现内容。Finder的标记赋予了用户更灵活管理文件的另一种方式，你既可以用它来标注文件的时效性、重要性，也可以用来定义自己的分类。每个文件是可以包含多个标记的，所以几种标注方式可以混用，文字和颜色也可以互补，标记的命名上建议使用你熟悉和直观的词语。  
Source: [Mac 软件面面观（二）文档管理](http://www.jianshu.com/p/0237546964af)  

	* 我把文件都装在哪里？怎么就直接开始`  $ xxx yyy zzz  ` 了？  
	> [Mac开发配置手册](http://aaaaaashu.gitbooks.io/mac-dev-setup/content/)
	* 管理员权限在哪些目录下需要 （比对 Windows 修改 C 盘下 Systems 文件）？  
	* sudo 的来龙去脉？  
	* 博客的标题是问题，正文就一行代码，是怎么个意思？  
	* 无数多程序员，学出来能给小白看的教程找得出来几个？可以不酱吗。    

* zsh  
密码又按错了，于是第一次
   
          Time to change your default shell to zsh!
          Changing shell for Ziyan.
          
   失败...  于是搜到 [网址](http://osxdaily.com/2012/03/21/change-shell-mac-os-x/)，输入

          $ chsh -s /bin/zsh

   就好了！  
   

* 最优与绕路  
本地发布 PDF 到底有几种方式，哪种最快最简单，是否一定要下载一个两个三个软件安装后才可以？  
背后的原理搞不清，问题解决也是稀里糊涂。稀里糊涂度过一个坑，再跳进另一个坑，似乎只有反反复复才可以终有一天知道，噢，原来是这样？  

* 实际上编程思维的语言特别简单，比如：
   
        Error: /usr/local/opt/makedepend not present or broken
   
   那就是 makedepend not present or broken. 可是不 Google 却很难完全确定到底是要我干什么对吧。于是难得人性化还会有一句提示说：
    
        Please reinstall makedepend. Sorry :(
       
   怎么 reinstall makedepend 却又是个障碍。我没有 install 过啊，怎么就 **RE**install 了呢？继续 Google，知道说，ok，那我应该：
   
        $ brew install makedepend
        
   还真是有一说一啊。==b 没理解这套语言和思路体系之前，真的觉得 WTF 噢！你造吗，get 与 geeeeet 不到就是一线之隔。Coder 不要总在线那边 呵呵呵呵呵 笑嘛。
      
### 所以，教程应该如何写？\* _Draft_

* Soft  
	* 首先，目的是什么。  
	* 其次，为什么要达到这个目的。  
	* 再次，如何达到这个目的。
	* 其他补充

* Hard  
	* 首先，这个软件解决什么问题。// Markdown 可以让使用简单符号让文字排版瞬间变好看！（加一点忽悠，引起兴趣，也激发大家更有动力去了解）  
	* 其次，这个软件是什么。  // Markdown 是一款轻量写作编辑器。（适当地历史沿袭背景介绍也可以有，但不能第一句就来这个啊，写作编辑器是什么？轻量如何定义？）
	* 再次，如何使用设个软件解决问题。// 相比 Word，相比 TXT 等的优势劣势、适用情景。（为什么用它不用它）
	* 最后，延伸。// 在 Chrome 里加插件可以blablabla。（读者根据自身时间、能力来决断是否接受）  

废话要不要咧？看个人风格。我觉得有一些来点染情绪就好，不必过多像是抒情文，不必过少像是机器人。  

* 其他问题
	* 如何平衡高大全、散布与简洁清晰。包括内容与引用。
	* 对读者水平应该有预估，并调整思路与内容。当然，预估很难准确。~~但若仅相信因人而异，放弃寻找普遍的大多数，这到底是对自身能力的怀疑，还是因有了 coder 身份的清高？~~// 比如，Pandoc（[Pandoc's Markdown 语法中文翻译](http://pages.tzengyuxio.me/pandoc/)）的介绍文档要不要首先包含与 Markdown 的语法同异对比？