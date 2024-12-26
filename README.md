# 示例结构
```bash
my-awesome-site/        # 网站根目录
│
├── _config.yml         # 配置文件，设置站点的基本信息，如标题、URL等
├── _data/              # 存放 YML 数据文件，常用于动态内容
│   └── navigation.yml  # 导航菜单配置
│
├── _includes/          # 存放页面片段和模板的目录
│   ├── header.html     # 网站头部（导航栏等）
│   ├── footer.html     # 网站底部
│   └── social-links.html # 社交媒体链接的公共部分
│
├── _layouts/           # 布局模板，控制站点页面结构
│   ├── default.html    # 默认布局模板
│   ├── home.html       # 首页布局
│   └── page.html       # 常规页面布局
│
├── _posts/             # 存放博客文章的文件夹
│   ├── 2023-12-24-my-first-robot.md # 博客文章1
│   └── 2023-12-25-an-introduction-to-ai.md # 博客文章2
│
├── _site/              # Jekyll 构建输出的静态文件（自动生成）
│   └── ...             # 这个目录是由 Jekyll 自动生成的，包含最终的HTML文件
│
├── assets/             # 存放静态资源的目录，如 CSS、JavaScript、图片等
│   ├── css/            # 自定义的CSS样式
│   │   ├── main.css    # 主要的CSS样式文件
│   │   └── _variables.scss # 用于自定义的SASS/SCSS变量
│   ├── js/             # 存放JavaScript文件
│   │   └── main.js     # 主要的JavaScript文件
│   └── images/         # 存放网站的图像资源
│       ├── logo.png    # 网站logo
│       └── hero-bg.jpg # 首页背景图
│
├── index.md            # 首页内容（Markdown格式）
├── about.md            # "关于"页面内容
├── projects.md         # 项目展示页面
└── 404.html            # 404错误页面
```

在 GitHub Pages 上托管静态网站时，目录结构的设置和文件命名非常重要。GitHub Pages 会自动识别名为 `index.html` 的文件作为默认入口文件。以下是详细的解释和示例：

### 单文件项目

如果你只有一个 HTML 文件，并希望它作为默认页面显示，那么将其命名为 `index.html` 放在仓库的根目录中即可。GitHub Pages 会自动识别并显示这个文件。

#### 示例目录结构

```
my-website/
│
├── index.html
└── README.md
```

在这种结构下，当你访问 `https://<username>.github.io/` 时，`index.html` 文件会自动加载并显示。

### 多文件项目

如果你有多个 HTML 文件，并希望它们可以通过不同的路径访问，你可以将这些文件放在不同的文件夹中。每个文件夹可以有自己的 `index.html` 文件，或者其他命名的 HTML 文件。

#### 示例目录结构

```
my-website/
│
├── index.html
├── about.html
├── contact.html
├── jianli/
│   └── index.html
└── README.md
```

在这种结构下：
- 访问 `https://<username>.github.io/` 会显示 `index.html` 文件。
- 访问 `https://<username>.github.io/about.html` 会显示 `about.html` 文件。
- 访问 `https://<username>.github.io/contact.html` 会显示 `contact.html` 文件。
- 访问 `https://<username>.github.io/jianli/` 会显示 `jianli` 文件夹中的 `index.html` 文件。

### 创建和推送文件夹

1. **创建文件夹和文件**：
   在你的本地仓库中，创建一个新的文件夹，并在其中添加 HTML 文件。例如，创建一个名为 `jianli` 的文件夹，并在其中添加 `index.html` 文件。

2. **推送到远程仓库**：
   将本地的更改推送到 GitHub 仓库。以下是基本的 Git 命令步骤：

   ```sh
   # 初始化Git仓库（如果还没有初始化）
   git init

   # 添加所有更改
   git add .

   # 提交更改
   git commit -m "添加简历页面"

   # 添加远程仓库（如果还没有添加）
   git remote add origin https://github.com/<username>/my-website.git

   # 推送更改到远程仓库
   git push -u origin main
   ```

3. **访问文件**：
   推送成功后，你可以通过以下URL访问你的文件：
   - `https://<username>.github.io/` 显示根目录中的 `index.html`。
   - `https://<username>.github.io/jianli/` 显示 `jianli` 文件夹中的 `index.html`。

通过这种方式，你可以轻松地管理和访问多个页面和文件。确保每个文件夹中都有一个 `index.html` 文件，以便能够直接通过文件夹路径访问。