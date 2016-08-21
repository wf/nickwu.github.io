---
title: Hello Blog
date: 2016-08-20 17:18:32
categories: blog
tags: [blog, hexo]
---
考虑了几个方案，最终还是决定使用 Hexo + github page 的方式，既方便、省钱又有好的服务。

简单地记录下使用过程：

## 快速入门

### 安装 Hexo command
``` bash
npm install -g hexo-cli
```
### 使用 Hexo 命令
可以简单的使用命令简写：
``` bash
hexo i [folder] # 初始化你的hexo目录
hexo n <title>  # 写文章
hexo g          # 生成静态页面
hexo d          # 部署 # 可与 hexo g 合并为 hexo d -g
hexo s          # 本地server，用于调试
```
详细的命令可以参考 [Hexo 文档][] 和命令行帮助：
``` bash
hexo --help
```

执行 new 命令时，将会生成指定名称的文章到 hexo\source\_posts\your-title.md。

如果想添加categories，以免每次手工输入，只需要在 hexo\scaffolds\post.md 文件添加一行，如下：
``` markdown
title: { { title } }
date: { { date } }
categories: 
tags: 
```

多标签请用格式： [tag1, tag2, tag3]

### 主题
比如使用 NexT，参见[Theme NexT 文档][]:
``` bash
git clone https://github.com/iissnan/hexo-theme-next themes/next
```
然后修改你的 hexo 目录的配置文件 _config.yml:
``` config
theme: next
```
在切换主题之后， 最好使用 hexo clean 来清除 Hexo 的缓存。

测试、调试时可以加 debug：
``` bash
hexo s --debug
```

### 配置 Deployment
先安装 hexo-deployer-git：
``` bash
npm install hexo-deployer-git --save
```
然后修改 hexo 配置文件的 deploy 字段，如：
``` config
deploy:
  type: git
  repo: git@github.com:yourname/yourname.github.io.git
  branch: master
```

#### 参考文档
1. [Hexo 文档][]
2. [hexo你的博客][]
3. [史上最详细的Hexo博客搭建图文教程][]
4. [如何在一天之内搭建以你自己名字为域名又具备cool属性的个人博客][]
5. [Theme NexT 文档][]
6. [Markdown 简明语法][]
7. [献给写作者的 Markdown 新手指南][]
8. [Markdown 语法说明][]
9. [Markdown 语法][]

[Hexo 文档]: <https://hexo.io/zh-cn/docs/index.html> "Hexo 文档"
[hexo你的博客]: <http://ibruce.info/2013/11/22/hexo-your-blog/> "hexo你的博客"
[史上最详细的Hexo博客搭建图文教程]: <https://xuanwo.org/2015/03/26/hexo-intor/> "史上最详细的Hexo博客搭建图文教程"
[如何在一天之内搭建以你自己名字为域名又具备cool属性的个人博客]: <https://wingjay.com/2015/12/07/%E5%A6%82%E4%BD%95%E5%9C%A8%E4%B8%80%E5%A4%A9%E4%B9%8B%E5%86%85%E6%90%AD%E5%BB%BA%E4%BB%A5%E4%BD%A0%E8%87%AA%E5%B7%B1%E5%90%8D%E5%AD%97%E4%B8%BA%E5%9F%9F%E5%90%8D%E7%9A%84%E5%BE%88cool%E7%9A%84%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/> "如何在一天之内搭建以你自己名字为域名又具备cool属性的个人博客"
[Theme NexT 文档]: <http://theme-next.iissnan.com/getting-started.html> "Theme NexT 文档"
[Markdown 简明语法]: <http://ibruce.info/2013/11/26/markdown/> "Markdown 简明语法"
[献给写作者的 Markdown 新手指南]: <http://www.jianshu.com/p/q81RER> "献给写作者的 Markdown 新手指南"
[Markdown 语法说明]: <http://wowubuntu.com/markdown/> "Markdown 语法说明"
[Markdown 语法]: <http://markdown.tw/#html> "Markdown 语法"
