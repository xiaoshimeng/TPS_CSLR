```linux
# 查看系统config
git config --system --list

# 查看当前用户（global）配置
git config --global --list

# 配置用户名
git config --global user.name "xiaolan"

# 配置邮箱
git config --global user.email  2717110178@qq.com

# 在当前目录新建一个Git代码库
git init

# 克隆一个项目和它的整个代码历史（版本信息）
git clone 链接地址
```

## 文件的四种状态

- **Untracked**：未跟踪，此文件在文件夹中，但没有加入git仓库，不参与版本控制，通过**git add**状态变为**Staged**
- **Unmodify**：文件已入库，未修改，此文件类型有两种去出，如果它被修改，变为**Modified**，如果使用**git rm**移除版本库，则成为**Untracked**文件
- **Modified**：文件已修改，仅仅是修改，两个去处，**git add**，进入暂存**staged**状态，使用**git checkout**，则丢弃修改，返回**unmodify**状态，即从库中取出文件，覆盖当前修改
- **Staged**：暂存状态，执行**git commit**则将修改同步到库中，这时库中的文件和本地文件变一致，文件为**Unmodify**状态，执行**git reset HEAD filename**取消暂存，文件为**Modified**

```Linux
# 查看制定文件状态
git status [文件名]

# 查看所有文件状态
git status

# 添加所有文件到暂存区
git add . 

# 提交暂存区中的内容到本地仓库 -m:提交的信息
git commit -m "信息"
```













