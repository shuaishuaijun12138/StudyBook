# StudyBook

这是一个多人合作的笔记分享

### 贡献者

<a href="https://github.com/2662419405" target="_blank">
    <img width=50 src="https://avatars2.githubusercontent.com/u/47957816?s=460&v=4">
</a>

<a href="https://github.com/2209951505" target="_blank">
    <img width=50 src="https://avatars3.githubusercontent.com/u/59152700?s=400&v=4">
</a>

<a href="https://github.com/2011111650" target="_blank">
    <img width=50 src="https://avatars0.githubusercontent.com/u/56377185?s=400&v=4">
</a>

<a href="https://github.com/1455516168" target="_blank">
    <img width=50 src="https://avatars1.githubusercontent.com/u/56419082?s=400&v=4">
</a>

<a href="https://github.com/lushengyunzuo" target="_blank">
    <img width=50 src="https://avatars0.githubusercontent.com/u/57390550?s=400&v=4">
</a>

<a href="https://github.com/Wangjiateng666" target="_blank">
    <img width=50 src="https://avatars3.githubusercontent.com/u/42726981?s=400&v=4">
</a>

> 提交代码或改进方案，被采纳的同学会出现在这里。欢迎更多的小伙伴们加入到我们的行列中(  •̆ ᵕ •̆ )◞♡

### 提交方式

1. 有想法的小伙伴可以fork我们的项目,然后pull request给我们
2. 在issues中,输入自己的用户名,我们会邀请你加入到我们的开发中^-^

###### 注意: 在分享笔记的时候,请以自己的名字在根目录下面创建文件夹,避免重复



#### 具体操作

> ###### 由于github是美国服务器,下载可能过慢,此步骤为加快下载速度,不在乎速度的可以跳过
>
> 1. 修改C:\Windows\System32\drivers\etc 下面的 hosts文件
>
> 2. 在原有文件的基础上,换行追加以下代码
>
>   3. ```
>  151.101.185.194 github.global-ssl.fastly.net
> 192.30.253.112 github.com
>  ```
> 4. 参考我的hosts文件为
>
> ```
> 127.0.0.1 localhost
> 151.101.185.194 github.global-ssl.fastly.net
> 192.30.253.112 github.com
> ```
> 6. 更新DNS缓存
>
>
> ```
> # macOS
> dscacheutil -flushcache
> # Windows
> ipconfig /flushdns
> ```
>
> 8. 成功之后
>

1. `git clone https://github.com/link58/StudyBook.git`  
2. `cd StudyBook`
3. 在目录下面创建自己名字的文件夹,例如`xxx`
4. 往文件夹里面添加内容
5. `git add .`
6. `git commit -m "此处添加描述信息" `
7. `git push origin master`
8. 完成

###### 注意 如果出现红字问题

```
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/link58/StudyBook.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```

解决

先输入->`git pull origin master`

再输入->`git push origin master`

###### 如果出现443报错,则是没有收到邀请,没有权限提交