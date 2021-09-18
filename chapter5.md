## 常见问题

### 1、执行命令 `git push origin master` 时，出现错误：remote: Permission to iambryanshen/xxx.git denied to xxx. fatal: unable to access 'https://github.com/xxx/xxx.git/': The requested URL returned error: 403

#### 解决方案

1、命令行进入到报错仓库文件夹根目录下
2、执行命令 `cd .git` 进入到 .git 文件夹目录下（.git 是隐藏文件）
3、执行命令 `vim config`
4、按 `i`，进入文件编辑模式
5、修改 

```
[remote "origin"]
url = https://github.com/iambryanshen/github-tutorial.git

为

[remote "origin"]
url = https://iambryanshen@github.com/iambryanshen/github-tutorial.git
```

6、按 `Esc`，c退出文件编辑模式
7、按 `Shift + :`
8、输入 `wq`
9、按 `Enter` 
10、尝试再次执行 `git push origin master`



