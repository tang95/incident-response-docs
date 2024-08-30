# PagerDuty 事件响应文档
[![Netlify 状态](https://api.netlify.com/api/v1/badges/ca66d085-7d5f-4a57-81c7-4eb104c9bdb7/deploy-status)](https://app.netlify.com/sites/incident-response-docs/deploys)

这是 PagerDuty 使用的事件响应流程的公开版本。它还用于为新员工准备随叫随到的职责，并提供不仅在准备事件时，而且在事件期间和之后应采取的行动的信息。有关此文档的更多信息及其存在的原因，请参阅[关于页面](docs/about.md)。

您可以直接在此仓库中查看文档[直接](docs/index.md)，或者以网站形式在 https://response.pagerduty.com 上查看。

[![PagerDuty 事件响应文档](screenshot.png)](https://response.pagerduty.com)

## 开发
我们使用 [MkDocs](https://www.mkdocs.org/) 从该仓库创建一个静态站点。

### 本地原生开发
对于在您的本地设备上进行开发，

1. 安装 [MkDocs](https://www.mkdocs.org/user-guide/installation/)。`pip install mkdocs`
1. 安装 [MkDocs PyMdown 扩展](https://squidfunk.github.io/mkdocs-material/extensions/pymdown/)。`pip install pymdown-extensions`
1. 如果您希望对任何代码示例进行语法高亮，请安装 [Pygments](https://pygments.org/)。`pip install pygments`
1. 安装 [PagerDuty MkDocs 主题](https://github.com/pagerduty/mkdocs-theme-pagerduty)。
    1. `git clone https://github.com/pagerduty/mkdocs-theme-pagerduty`
    1. `cd mkdocs-theme-pagerduty & python3 setup.py install`
1. 要在本地测试，请从项目目录运行 `mkdocs serve`。
1. 现在您可以在浏览器中查看网站，网址为 `http://127.0.0.1:8000`。网站将自动更新，当您编辑代码时。

### Docker
对于使用 Docker 进行本地开发，

1. 构建 Docker 镜像并立即加载使用。`docker build --load -t mkdocs .`
1. 运行容器并传递您当前的工作目录。`docker run -v $(pwd):/docs -p 127.0.0.1:8000:8000 mkdocs`
1. 现在您可以在浏览器中查看网站，网址为 `http://127.0.0.1:8000`。网站将自动更新，当您编辑代码时。

_注意：如果您使用的是 Apple Silicon 设备，请在 `docker build` 命令中添加 `--platform linux/arm64/v8`，以获取原生 Apple Silicon 镜像。这将比翻译 arm64 镜像更快。_

## 部署
1. 运行 `mkdocs build --clean` 以生成用于上传的静态站点。
1. 将 `site` 目录上传到 S3（或您希望托管的任何地方）。

        aws s3 sync ./site/ s3://[BUCKET_NAME] \
          --acl public-read \
          --exclude "*.py*" \
          --delete

## 许可证
[Apache 2](https://www.apache.org/licenses/LICENSE-2.0)（参见 [LICENSE](LICENSE) 文件）

## 贡献
感谢您考虑贡献！如果您有任何问题，尽管问 - 或者直接提交您的问题或拉取请求。最坏的情况是我们会礼貌地请您更改某些内容。我们欢迎所有友好的贡献。

以下是我们首选的提交拉取请求的流程，

1.  fork 它（ https://github.com/PagerDuty/incident-response-docs/fork ）
1.  创建您的功能分支（`git checkout -b my-new-feature`）
1.  提交您的更改（`git commit -am '添加某些功能'`）
1.  推送到分支（`git push origin my-new-feature`）
1.  创建一个新的 Pull Request。