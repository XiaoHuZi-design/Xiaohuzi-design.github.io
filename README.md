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

