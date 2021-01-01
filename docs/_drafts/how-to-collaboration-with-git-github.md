---
title: 如何使用 Git/GitHub 协作
author: 杨凯
---

![GitHub flow](../assets/img/github-flow.png)

> GitHub flow 的核心优势在于其流程带来的自动化可能性，能够做到其它流程无法实现的检查过程，并极大简化开发团队的体力劳动，真正发挥自身的价值。  

本文的基础参考自 GitHub 官方推荐的 [GitHub flow](https://guides.github.com/introduction/flow/)，在阅读之前可以先看看官方文档，以确保更好的阅读体验。  

## 1. 工作的基础
分支是 Git 的核心，也是 GitHub 工作流的基础。只有一个规则：`main` 分支上的所有东西都必须是可靠的。  

所以在本地修改仓库时一定要新建一个分支，取一个有意义的分支名，以便在后面的协作环节让其他人能更快地知道你在尝试做什么。  
<br>

## 2. 创建一个讨论
如果你在自己的分支中碰到一个问题，或者是希望能有其他人一起来完成这个分支的开发，那么你就可以将这个分支推送到 GitHub 上：  
```bash
# 一定要取一个有意义的分支名，这样可以让别人知道这个分支有什么用
git push origin my_branch:my_branch
```

然后在 GitHub 上创建一个 PR，也就是 Pull requests，直译过来是“拉取请求”，然会就会 GitHub 就会比较这两个分支，所有人都可以看到它们的不同，比起单纯的分支来说，PR

## 3. 合并到主分支