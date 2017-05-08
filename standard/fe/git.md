# Git使用规范

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


- Tips

>  * **git cz**: [Commit message 和 Change log 编写指南]((http://www.ruanyifeng.com/blog/2016/01/commit_message_change_log.html))
>  * **git stash**: [用于保存和恢复工作进度，这里有个细节要注意，文件暂存不区分分支]((https://gist.github.com/subchen/3409a16cb46327ca7691))


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


