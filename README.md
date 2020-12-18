# BBS: 轻量级论坛系统

## 项目简介
BBS 是一个简介好用的论坛，在BBS上，你可以浏览丰富多彩的主题论坛，浏览他人的帖子，评论他人的帖子，当然也可以通过帖子的形式分享你所想要分享的；如果不想让别人知道你的名字，每个论坛都有树洞，在树洞里所有的帖子都是匿名的；同时你也可以创建属于自己的论坛，邀请你的好友加入你的论坛进行讨论，如果你不想公开你们的讨论，论坛支持私有创建，其中的内容只有论坛成员才可见。

## 技术栈
前端：使用基于 `React` 的 `Next.js` 框架    
后端：
- 服务端：用 golang 编写的web框架 `gin`
- 数据持久化：
  - 结构化数据：mysql
  - 非结构化数据：minio


## 项目部署方式
要部署该项目，有两种主要方式：

### 方法1: 通过 docker，docker-compose 部署(推荐)
- 前提条件：
  - 1. 在您的机器上已经配置了 docker 环境，并且 docker daemon 正在运行
  - 2. 3000 端口和 5000 端口没有被占用

- 部署方法：
  
首先进入`bbs_doc`目录
```
cd bbs_doc
```

然后在终端下输入：
```
docker-compose up
```
可能拉取镜像要花费一些时间。
然后访问 `http://localhost:3000/users/login` ，即可进入 bbs.

### 方法2: 通过分别编译运行前后端来运行

- 前提条件：
  - 1. 你的机器上有 `golang 1.14` 环境，并且开启 `GO111MODULE`; 您的机器上有 `node:14` 环境，并且包管理器 `yarn, npm` 可用。
  - 2. 3000 端口和 5000 端口没有被占用

- 部署方法：

  - 后端：
    - 首先下载后端项目：
    ```
    git clone https://github.com/service-computing-2020/bbs_backend.git
    ```
    - 然后进入项目根目录, 运行项目：
    ```
    cd bbs_backend
    go run main.go
    ```

  - 前端：
    - 首先下载前端项目：
    ```
    git clone https://github.com/service-computing-2020/bbs_frontend.git
    ```
    - 然后进入项目根目录，下载依赖：
    ```
    cd bbs_frontend
    yarn install
    ```
    - 编译项目：
    ```
    npm run build
    ```
    - 运行：
    ```
    npm run start
    ```
## API 文档访问方式

在您的浏览器（推荐火狐浏览器，谷歌浏览器可能会因为“不安全的”原因无法访问）输入：`http://bobby.run:30086/swagger/index.html`, 可以看到如下的画面：
![](https://tva1.sinaimg.cn/large/0081Kckwgy1gls0gamz1sj31ba0u01ap.jpg)
将图中红色框的地址更换为：`http://bobby.run:30086/swagger/doc.json`, 可以看到：
![](https://tva1.sinaimg.cn/large/0081Kckwgy1gls0icm9pkj31ba0u0h7q.jpg)
下面便是我们本次后端的所有 API。

## 前端界面展示


## 后端设计










