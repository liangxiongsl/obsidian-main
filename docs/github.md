
### 基本命令
```
# （全局）配置 git
git config --global user.name "用户名"
git config --global user.email "邮箱地址"

# 初始化新的本地仓库
git init

# 添加文件（将文件运到货车上）
git add [文件]
# 添加所有更改过的文件
git add .

# 提交更改（将货车运到本地仓库）
git commit -m "提交信息"

# 查看仓库状态，提交历史
git status
git log

# 推送更改到 github 远程仓库（将文件从本地仓库传送到远程仓库）
git push origin [分支名]

# 拉取远程仓库的更改到本地仓库
git pull origin [分支名]

# 克隆某个仓库
git clone https://github.com/用户名/仓库名.git
```


### 常见命令块

#### 首次配置

```
git config --global user.name "liangxiongsl"
git config --global user.email "1506218507@qq.com"
```

#### 将本地文件同步到github进行存储

首次建库
```
# 首先用 github 的客户端或web端创建一个仓库 repo

git init

git add .

git commit -m "first commit"

git branch -M main

git remote add origin https://github.com/liangxiongsl/repo.git

git push origin main
```
注：一般不直接提供超过 100m 的文件上传


更新
```
git pull origin main
```



