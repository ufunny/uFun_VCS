## 0. 背景:   
__μfun 项目组已经确定使用 Github 来作为 μfun 项目软件部分代码托管平台.__       

## 1. 版本管理简介:    

>    什么是版本控制？我为什么要关心它呢？版本控制是一种记录一个或若干文件内容变化，以便将来查阅特定版本修订情况的系统。在本书所展示的例子中，我们仅对保存着软件源代码的文本文件作版本控制管理，但实际上，你可以对任何类型的文件进行版本控制。    
    
>    如果你是位图形或网页设计师，可能会需要保存某一幅图片或页面布局文件的所有修订版本（这或许是你非常渴望拥有的功能）。    
    
>    采用版本控制系统（VCS）是个明智的选择。有了它你就可以将某个文件回溯到之前的状态，甚至将整个项目都回退到过去某个时间点的状态。    
    
>    你可以比较文件的变化细节，查出最后是谁修改了哪个地方，从而找出导致怪异问题出现的原因，又是谁在何时报告了某个功能缺陷等等。使用版本控制系统通常还意味着，就算你乱来一气把整个项目中的文件改的改删的删，你也照样可以轻松恢复到原先的样子。但额外增加的工作量却微乎其微。([Ctrl+C](https://code.csdn.net/help/CSDN_Code/progit/zh/01-introduction/01-chapter1))    
     
 - __~~Local VCS 本地版本管理:~~__
  ![](https://code.csdn.net/CSDN_Code/progit/blob/master/figures/18333fig0101-tn.png)
--
 - __~~Central VCS 集中式版本管理:~~__
![](https://code.csdn.net/CSDN_Code/progit/blob/master/figures/18333fig0102-tn.png)
--
 - __Distributed VCS 分布式版本管理__:     
    > git 即属于此种方式.     

![](https://code.csdn.net/CSDN_Code/progit/blob/master/figures/18333fig0103-tn.png)
--

### 2. Git 资料:     

> -  [Git 官网](http://git-scm.com/)    

> -  __这里还有一个非常不错的流程图教程, 会非常受用. [Git Cheatsheet](http://ndpsoftware.com/git-cheatsheet.html#loc=index;)__  __十分推荐!__     

> -  [廖雪峰: Git 教程](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000), 国内的一位大拿. 做的很不错, 另外那个 python 做的也挺好, 可惜我没坚持学完. 半吊子了. 可惜.    
    
> -  [Pro Git，作者Scoot Chacon. Git官网唯一参考书.Pro Git book(简体中文版)](http://git-scm.com/book/zh/v1)    
    
> - [OSChina 的 Pro Git 中文版](http://git.oschina.net/progit/index.html) 这个版本和上面的那个一样. 不过更清爽一些.     
    
> -  嫌繁琐的话, 这里有个简化版本的, 基本满足要求. 深入的话再看 Pro Git Book. [CSDN CODEProgit中文版](https://code.csdn.net/help/CSDN_Code/code_support/Progit_Index)
    
> - 这个是 github 官方给的教程, git 的常用功能. [github-git-cheat-sheet.pdf](https://training.github.com/kit/downloads/github-git-cheat-sheet.pdf)    
    

#### 2.1 Git 客户端安装.    
> 鉴于大家基本都用windows,  这里推荐安装 windows 下的客户端 mysysgit + TortoiseGit.     

#### 2.2 Github 客户端.    
> [windows客户端不支持 XP](https://help.github.com/articles/windows-xp-is-not-supported/). 用 XP 的要慎重了. 用 TortoiseGit 吧. 哈哈       
> > - [如何高效利用GitHub](http://www.yangzhiping.com/tech/github.html)      
    
> 如果想安装 Github for windows 客户端的话, 就不需要安装 msysgit 和 TortoiseGit 了.     

    > - [TortoiseGit和msysGit安装及使用笔记（windows下使用上传数据到GitHub）](http://blog.csdn.net/chinaonlyqiu/article/details/8826767)
    > - TortoiseGit 在 google 的 code 上, 不翻墙可能上不了. 所以, 我下载下来放到 **百度网盘** 了, 基本都是最新版(2014-12-25 22:50:29): __[分享: Git&Github版本管理软件工具包-12.25    戳这里下载必要的软件](http://pan.baidu.com/s/1o6BOnrk)__    
    > - 先安装 TortoiseGit 再安装中文包 LanguagePack. 根据情况选择 32bit 和 64bit. 
    > -  安装完之后就是配置了.    

    >  > 这个可以再百度或者谷歌搜到一大堆, 我就不重复叙述了. 个人建议用 [Github 官方的帮助文档](https://help.github.com/). 里面基本有你所有想要了解的东西.     

    >  > 比如:    
    >  > - [设置用户名和邮箱](https://help.github.com/articles/set-up-git/)      
    >  > - [安装完 Github for windows 还需要安装其他东西吗?](https://help.github.com/articles/do-i-need-to-install-anything-extra/)
    >  > - [安装完 Github或者 TortoiseGit 之后还需要项目公钥吗?](https://help.github.com/articles/do-i-need-ssh-keys-to-use-github-for-windows/)    
    > 建议不要用 SSH 公钥, 没必要, 麻烦. 现在基本都用 https. 客户端都会缓存你的认证信息, 等你输入一次之后, 基本以后都不需要再重新输入 . 
    >  > - [Github for windows 客户端帮助](https://help.github.com/categories/github-for-windows/)

## 3. markdown 
>  由于 markdown 的实现各个平台有细节差异. 所以, 还是参照 Github 官方的 help 文档来学习比较有针对性. 还好内容不错. 可以很快上手.    

>   > -  [基础知识](https://help.github.com/articles/markdown-basics/)        

>   > -  [github 对 markdown 特色功能](https://help.github.com/articles/github-flavored-markdown/)    
>   > -  [Writing on GitHub](https://help.github.com/articles/writing-on-github/)      

>   > - [[译] GitHub 风格的 Markdown 语法](https://github.com/cssmagic/blog/issues/13)      

>   > -  [Markdown写作浅谈](http://www.yangzhiping.com/tech/r-markdown-knitr.html)        

>   > - [献给写作者的 Markdown 新手指南](http://www.jianshu.com/p/q81RER)    

>   > - [Markdown语法说明(台湾-繁体中文)](http://markdown.tw/)     

>   > - [Markdown 语法说明 (简体中文版)](https://github.com/riku/Markdown-Syntax-CN/blob/master/syntax.md)    

>   > - [Markdown 语法简体中文版](https://github.com/riku/Markdown-Syntax-CN)     
整个项目的 Github 链接.     

>   > - __[windows 下推荐使用 markdownpad ](http://markdownpad.com/)__    
来编写 markdown 文档, 可以离线编写, 实时预览, 不过高级版需要购买, 有钱的话就支持正版.    

>   > - [这个是在线具有实时预览功能的 markdown 编辑器](http://jbt.github.io/markdown-editor/)    
    
## 4. License 选择
> 抛出几张图,  我也不大懂. 逃)       

>  ![](http://image.beekka.com/blog/201105/bg2011050101.png)   
>  ![](http://hi.csdn.net/attachment/201105/25/0_1306296079vEDZ.gif)
>  ![](http://hi.csdn.net/attachment/201105/25/0_13062960880Uov.gif)


-------
## 5. 后记    
__水平有限, 我只是 google/Baidu 的搬运工, 这些资料都是我曾经学习时用到的, 但是 Git 和 Github 用的不多, 所有有问题大家一起讨论互相学习共同进步.__      

> 如果哪里有遗漏的, 可以提出来我来补充.     

---
>  * By MingH
 * Email: omonkerman@qq.com
 * QQ: 401330597    
---   


---  
    
