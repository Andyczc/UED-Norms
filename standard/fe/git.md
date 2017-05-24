# Git使用规范
[Git中文教程](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)

## 操作规范

### 流程图
**更新远程仓库代码**:
```flow
st=>start: git pull --rebase
e=>end
co=>operation: No Conflict
sub1=>operation: merge Conflict
sub2=>operation: git add .
sub3=>operation: git rebase --continue

cond=>condition: Yes or No?

st->co->cond
cond(no)->sub1(right)->sub2(right)->sub3(right)->co
cond(yes)->e

```


-------------------

**提交代码到远程仓库**:
```flow
st=>start: git add .
e=>end: git push

cz=>operation: git cz

pl=>start: git pull --rebase
co=>operation: No Conflict
sub1=>operation: merge Conflict
sub2=>operation: git add .
sub3=>operation: git rebase --continue

cond=>condition: Yes or No?

st->cz->pl->co->cond
cond(no)->sub1(right)->sub2(right)->sub3(right)->co
cond(yes)->e

```



## 仓库/分支管理

### 流程图

**提交代码到远程仓库**:
```flow
st=>start: 种子工程
e=>end: 发布上线

program=>operation: 项目工程
program

master=>operation: 默认分支(弃用) 
master
dev=>operation: 开发分支 
dev
feature1=>operation: 新功能分支1
feature1
feature2=>operation: 新功能分支2 
feature2...
staging=>operation: 稳定分支 
staging
deploy_script=>operation: 发布分支 
deploy_script

cond1=>condition: 使用 or 废弃?
cond2=>condition: 新开分支流程 or 发布流程?

st->program->cond1
cond1(no,left)->master
cond1(yes,right)->dev->cond2
cond2(no,left)->staging->deploy_script->e
cond2(yes,right)->feature1->feature2(left)->dev

```

## 分支管理
分支管理规范仅作用于UED下前端组。

### 研发新项目
- UED主管牵头在dev分支完成构建工程、主代码框架的建设
- 前端开发工程师统一在dev分支进行开发、测试
- 开发人员在开始每天的研发工作前，必须先更新远程仓库代码到本地，每天下班后，必须将本地可提交代码提交到远程代码仓库


### 迭代现有项目
在迭代现有产品时，前端开发工程师应该：

- 更新生产环境分支(staging)代码到本地，并基于staging分支新开分支进行开发,命名规则为“feat-分支类型（修复BUG、新功能）-分支功能（登录bug、报表模块）”
    ```
        // 切换到staging分支
        git checkout staging

        // 更新远端代码到本地
        git pull --rebase

        // 基于staging分支新开修复BUG分支
        git checkout -b feat-fix-login-bug

        // 基于staging分支新开新功能分支
        git checkout -b feat-reports
    ```
- 在该新分支完成所有研发工作以后，前端应该将该分支代码合并到dev分支，并且必须在dev分支验证自己研发的所有功能，并通知前端组其他成员注意，确认无误后通知UED主管安排提测

    ```
        /* 合并 feat-reports 分支到dev*/

        // 切换到dev分支
        git checkout dev

        // 更新远程仓库代码到本地
        git pull --rebase

        // 将feat-reports合并到dev
        git rebase feat-reports
        
        /* 合并报冲突 */
        // CONFLICT (content): Merge conflict in xxxx.js
        // CONFLICT (content): Merge conflict in xxxx.css
        // CONFLICT (content): Merge conflict in xxxx.js
        
        // 解决此次冲突后，添加修改到版本库
        git add .

        // 不用commit，直接执行下一次rebase合并
        git rebase --continue

        // 如果还有冲突，继续上面的操作，直到合并完成

        // -------------------------------------------
        // 跳出rebase
        git rebase abort

        // 确认冲突解决好了，但是执行git rebase --continue 失败，
        // 可以跳过本次冲突解决，直接进入下一条合并
        git rebase --skip

    ```





- 在本次研发任务上线稳定之后，前端开发工程师才可以删除该分支

    Tips

    > * **git cz**: [Commit message 和 Change log 编写指南]((http://www.ruanyifeng.com/blog/2016/01/commit_message_change_log.html))
    > * **git stash**: [用于保存和恢复工作进度，这里有个细节要注意，文件暂存不区分分支]((https://gist.github.com/subchen/3409a16cb46327ca7691))
    > * [git rebase 与 git merge 合并分支的区别](http://blog.jobbole.com/84664/)
    > * 前端开发人员应该养成每完成一个小功能、修复一个小bug之后就提交一次commit的习惯，避免因为一次改动太多造成大规模的冲突


## 仓库管理
| 仓库名称      |    用途 |
| :--------: | --------|
|   zmfe-shop | 开发环境仓库  |
|   zmfe-shop-node | UED自己搭建的NODE服务器仓库，用于代理转发，mock数据等  |
|   zmfe-shop-test<br> or<br> zmfe-shop-fe|  生成环境代码仓库，用于提供测试，发布上线 |
