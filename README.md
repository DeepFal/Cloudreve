# 部署步骤
#### 步骤一：克隆我的 GitHub 仓库

1. **克隆仓库**：将以下仓库克隆到你的 GitHub 账户中。

https://github.com/foss-android/Cloudreve

#### 步骤二：设置 GitHub Actions 权限

1. **配置权限**：
  * 进入你克隆的仓库，点击页面顶部的 “Settings”。
  * 在左侧边栏中选择 “Actions” > “General”。
  * 找到 “Workflow permissions” 部分，选择 “Read and write permissions” 以确保工作流有足够权限运行。
  * 保存更改。

#### 步骤三：运行工作流

1. **启动 GitHub Actions**：
  * 返回你的仓库主页，点击 “Actions” 标签。
  * 找到预配置好的工作流并启动。仓库中的工作流文件已经配置好，并且所有提示都是中文，非常友好易懂。

#### 步骤四：部署到抱抱脸空间

1. **创建一个抱抱脸空间**：
  * 打开 [抱抱脸空间](https://huggingface.co/spaces)，创建一个新的空间。
2. **创建 Dockerfile**：
  * 在抱抱脸空间内创建一个名为 `Dockerfile` 的文件。
3. **编辑 Dockerfile 文件内容**：
  * 将以下内容写入 `Dockerfile` 文件中：

```
FROM ghcr.io/[你的 GitHub 用户名]/[Fork 的仓库名]:latest
```

  * 例如，如果你的 GitHub 用户名是 `yourname`，而克隆的仓库名是 `cloudreve-repo`，内容应为：

```
FROM ghcr.io/yourname/cloudreve-repo:latest
```
4. **修改 README.md 文件**：
  * 将抱抱脸空间中的 `README.md` 文件内容全部删除，并替换为以下内容：

```
title: Cloudreve
emoji: 📚
colorFrom: pink
colorTo: yellow
sdk: docker
pinned: false
app_port: 8080
```

  * 这段内容将设置空间的各种基本属性。

### 总结

通过这些步骤，你可以轻松克隆我的 GitHub 仓库，并将 Cloudreve 部署到抱抱脸空间中。你只需安排正确的 `Dockerfile` 和 `README.md` 文件内容即可，无需额外的繁琐修改。
[/quote]
