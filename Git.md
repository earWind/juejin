# Git Flow工作流
## 特点
### 1.项目存在两个长期分支
* 主分支master
* 开发分支develop
>> ![](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/34346cb869464c9fa43621236e594696~tplv-k3u1fbpfcp-watermark.image)

前者用于存放对外发布的版本，任何时候在这个分支拿到的，都是稳定的分布版；后者用于日常开发，存放最新的开发版。
### 2.项目存在三种短期分支
* 功能分支（feature branch）
* 补丁分支（hotfix branch）
* 预发分支（release branch）

一旦完成开发，它们就会被合并进develop或master，然后被删除。
>> ![](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/f5e577f5076e436d921be9a8f7627490~tplv-k3u1fbpfcp-watermark.image)

[了解Git Flow](https://nvie.com/posts/a-successful-git-branching-model/)  
[Git分支管理策略](http://www.ruanyifeng.com/blog/2012/07/git.html)  
[Git Flow 的正确使用姿势](https://www.jianshu.com/p/41910dc6ef29)