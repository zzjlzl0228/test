# GIT 和 github

- 可以使用 git 工具向 github 上上传代码
- 可以拉取 github 上面的代码



## 什么是 github

- 他是一个网站
- 第一个功能： 是一个社区网站
  - 展示一些新技术
  - 展示一些插件
- 第二个功能：远程仓库
  - 记录你每一次的变化
  - 时光倒流
- 你想王 github 上传代码
  - 第一个就是有一个 GitHub 的账号
  - 第二个就是你的电脑要有 git 这个工具



## 什么是 git

- 他是一个软件
  - 他不是一个安装完毕能在桌面出现一个图标的软件（是一个基于操作系统的软件）
  - 他是一个依靠命令行来操作的软件
  - 他是一个专门用来管理你本地文件夹的软件
  - 还有一个功能就是 把本地管理的文件夹上传到 github
    - 第一个就是 github 的账号
    - 第二个就是有 git 这个软件
    - 第三个就是当前这个文件夹要被 git 管理着
  - 中文名称： 版本管理器
    - 版本 ： x.y.z
    - x： 大版本
    - y： 主要功能的更新
    - z： 日常的更新迭代



## 申请一个 github 账号

- 打开 [github](httpd://github.com) 网站
- 点击 `sign up`
- 填写用户名、邮箱、密码
- 选择 free
- create
- 会收到一个邮件，去邮箱中点击验证





## 安装 git

- 下载 git

  - 来到 [官网](https://git-scm.com/)
  - 点击 `download`

- 安装

  - 找到 安装包，双击安装
  - 安全选择 `是`
  - 一路 `next`最后 `INSTALL`

- 检测安装成功

  - 任意一个地方鼠标右键单击，只要有 `git bash here` 就行

- 检测版本号

  - 打开控制台
  - cmd
  - prowershell
  - gitbashhere
  - 输入指令 `$ git --version`

- 首次安装需要进行一次配置

  - 查看配置项

    ```shell
    # 打开命令行窗口
    $ git config --list
    # 这个指令是查看当前配置列表的
    ```

  - 配置用户名

    ```shell
    # 打开命令行窗口
    $ git config --global user.name "guoxiang"  # 可以选择电脑主机名称或者github用户名
    # 这个指令是配置全局用户名
    ```

  - 配置邮箱

    ```shell
    # 打开命令行窗口
    $ git config --global user.email "dpd223322@163.com"  # 注册 github 的时候的邮箱
    # 这个指令是配置全局邮箱的
    ```



## git 管理你的文件夹

- 想让 git 管理那个文件夹就打开到哪个文件夹目录

- 让 giit 管理你的文件夹

  ```shell
  # 使用 指令 的形式让 git 管理你的文件夹
  $ git init
  # 这个指令是初始化当前文件夹，经过初始化的文件夹就被 git 管理了
  ```

  ​

## 上传代码

1. 你要选择那些文件上传

   - 哪些不能上传（空文件夹）

   - 选择上传的文件

     ```shell
     # 选择上传单个文件
     $ git add readme.md
     # 选择单个文件夹
     $ git add demo/
     # 选择文件夹中所有内容
     $ git add .
     ```

   - 会把你选择到的文件或者文件夹存储到暂存区

2. 对本次上传所以个说明

   ```shell
   # 依靠指令做一个说明
   $ git commit -m "我本次只上传了一个 readme 文件"
   ```

3. 你要告诉你的 git 你上传到哪里

   - 管理一下 github

   - 来到 github 准备一个仓库，用来存储当前这个本地文件夹

     ```shell
     # 关联一个仓库地址
     $ git remote add origin https://github.com/guoxiang920322/heima65first.git
     # 这个指令是关联一个仓库地址的
     ```

4. 上传代码到 github

   - 依旧是使用指令上传

     ```shell
     # 当前的本地文件夹第一次推送的时候
     $ git push -u origin master
     # 当前的本地文件夹第二次及以后推送的时候
     $ git push
     ```

5. 第二次提交

   1. 第一步是选择文件

      `$ git add .`

   2. 第二部是说明 `$ git commit -m "说明"`

   3. 直接提交




## 下载代码

- 第一次下载代码

  - 找到对应的远程仓库

  - 选择一个位置来保存你下载的东西（下载下来的就是一个文件夹）

  - 拉取代码

    ```shell
    $ git clone https://github.com/guoxiang910223/heima65first.git
    # 这个指令是克隆仓库到本地
    ```

- 第二次下载代码

  - 来到第一次克隆过的文件夹内部，打开 git bash

  - 拉取代码

    ```shell
    # 第二次及以后拉去代码使用
    $ git pull
    ```

    ​