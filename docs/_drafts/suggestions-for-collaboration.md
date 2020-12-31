---
title: 一些关于协作的建议
author: Jax Yang
---

> 每个较大的开源项目都有自己的风格指南: 关于如何为该项目编写代码的一系列约定 (有时候会比较武断). 当所有代码均保持一致的风格, 在理解大型代码库时更为轻松.  
> ——[Google 开源项目风格指南（中文版）](https://google-styleguide.readthedocs.io/zh_CN/latest/)  

因为我们每个人都有自己的编程风格，比如命名习惯，这些风格并没有绝对的优劣之分。但是当我们在同一个仓库协作时就必须（或者说应该）考虑到项目中的其他人，一个人人都遵守的规范会极大地减少团队间沟通的成本，也会对项目的开发有利。就拿我自己来说，以前我没有重视编程规范，写代码十分随意，这样造成的后果就是当我过一段时间再来看我的代码时会觉得晦涩难懂，但是当我有意识地遵循一些规范后，代码不仅更易懂了，效率也有提高。  

你可能注意到了，这篇文章的题目并不是“关于协作的规范”，而是“关于协作的建议”。项目的规范十分重要，但与此同时也很难编写，尤其是对于我们这些没有什么开发经验的菜鸟来说，所以本文的目的不是给出一个完美的规范要求必须遵守，而是抛砖引玉给出一些建议，并且通过讨论来决定是否有必要（或有价值）来遵守。  

## 一些建议
再次重申这只是一些个人的建议，能不能转化成规范还要看大家的参与，我希望大家都能参与进规范的编写，让我们的开发更加高效。  

### 0. 规范的分类
___
姑且先将规范粗暴地分为 3 类：  
1. ❗ 强制  
    一般用于对项目维护影响很大的方面，比如文件目录的结构  

2. ⭕ 推荐  
    一般用于对项目维护有影响但不是非常大，同时有利于成员沟通，比如文件的命名格式  

3. ❌ 严禁  
    一般用于对项目有害的行为，比如随意在仓库里存放无关文件  

### 1. 计划编写的规范
___
- [ ] 如何使用本仓库（小组博客）  
- [ ] 如何使用 Git/GitHub 协作（可参考 GitHub 工作流）  
- [ ] 如何编写项目日志  
- [ ] 我们的文档规范  

### 2. 如何使用本仓库（小组博客）
___
值得注意的是本仓库的主分支是 `main`，为 GitHub Pages 指定的主目录是 `main` 分支下的 `docs/`。  

本仓库的目录结构大致如下：  
- docs（Jekyll 博客文件的主目录）  
    - _drafts（用于存放草稿）  
    - _posts（用于存放博客文章）  
    - assets（用于存放资源文件，如图片）  
    - _config.yml（Jekyll 的配置文件）  
    - .gitignore  
    - 404.html  
    - about.md  
    - Gemfile   Gemfile.lock  
- README.md（使用仓库前必须阅读的文档）  

其中比较重要的就是 `_posts` 目录，其他的大都不需要修改，除非是要为博客网站增加新功能或重构。关于博文的编写要求其实不多，主要就是一下几点：  
1. ❗ 博文必须放在 `/docs/_posts/` 目录下，不然 Jekyll 不会识别或导致其他问题  

2. ❗ 修改文件时必须在自己的分支中进行，确认无误后再合并到主分支进行推送  

3. ⭕ 博文的文件名只能包含数字、英文小写、短横线 `-` 以及 `.`，不能使用汉字，正确的示例：`2020-12-31-a-blog-post.md`  

4. ❌ 不要将本地用于测试的配置文件推送到仓库  

其实我们编写的 md 文件并不是最后的网页文件，在我们推送到仓库后，GitHub 的 Jekyll 会自动根据配置文件生成相应的网页文件，所以看起来会比纯的 Markdown 丰富很多，所以要小心对待配置文件，因为可能会影响到 Jekyll 的正常运行。  

### 碎碎念