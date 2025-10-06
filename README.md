# 学术个人主页

这是一个极简、专业的学术个人主页模板，参考顶级经济学者的主页设计，可以轻松托管到 GitHub Pages 上。

## 特点

- ✨ 极简专业的设计风格
- 📱 完全响应式布局，支持移动设备
- 🎯 左侧边栏 + 右侧内容的经典布局
- 📚 按研究主题分组展示论文
- 🚀 易于自定义和部署
- 💡 无需复杂的 JavaScript，纯 HTML + CSS

## 快速开始

### 1. 创建 GitHub 仓库

1. 登录 GitHub
2. 创建一个新仓库，命名为 `username.github.io`（将 `username` 替换为你的 GitHub 用户名）
3. 勾选 "Public" 公开仓库

### 2. 上传文件

将以下文件上传到你的仓库：
- `index.html` - 主页文件
- `styles.css` - 样式文件
- `README.md` - 说明文档（可选）

### 3. 启用 GitHub Pages

1. 进入仓库的 **Settings（设置）**
2. 在左侧菜单找到 **Pages**
3. 在 **Source** 部分，选择 `main` 分支
4. 点击 **Save（保存）**
5. 几分钟后，你的网站将在 `https://username.github.io` 上线

## 自定义指南

### 修改个人信息

编辑 `index.html` 文件，找到以下部分并修改：

#### 基本信息（第21-27行）
```html
<h1 class="name">您的姓名</h1>
<div class="title">
    <p>职称</p>
    <p>院系名称</p>
    <p>大学名称</p>
</div>
```

#### 联系方式（第29-38行）
```html
<p><strong>邮箱：</strong><br>
<a href="mailto:email@university.edu">email@university.edu</a></p>

<p><strong>地址：</strong><br>
建筑名 房间号<br>
街道地址<br>
城市, 省份 邮编</p>
```

### 添加个人照片

1. 创建 `image/` 文件夹
2. 准备一张个人照片（建议尺寸：400x400 像素以上）
3. 将照片命名为 `profile.jpg` 或 `profile.png`
4. 上传到 `image/` 文件夹
5. 照片会自动显示（无需修改代码）

### 添加研究主题和论文

本模板采用**按主题分组**的方式展示研究，而非传统的按发表状态分类。

#### 添加研究主题（第51-74行）

```html
<div class="topic">
    <h3 class="topic-title">主题：您的研究方向</h3>
    <p class="topic-description">
        简要描述这个研究主题的背景、动机和意义。
    </p>
    
    <div class="paper">
        <div class="paper-header">
            <strong class="paper-title-bold">论文标题</strong>
            <span class="coauthors">(与合作者姓名)</span>
            <span class="journal-status">期刊缩写或状态</span>
        </div>
        <p class="paper-question">这篇论文要回答什么核心问题？</p>
    </div>
</div>
```

#### 期刊状态示例
- 已发表：`AER`, `JPE`, `QJE`, `Econometrica` 等
- 审稿中：`审稿中`, `under review`, `R&R`
- 工作论文：`工作论文`, `working paper`

### 管理 PDF 文件

建议创建一个 `papers` 文件夹来存放所有论文 PDF：

```
your-repo/
├── index.html
├── styles.css
├── profile.jpg
├── cv.pdf
└── papers/
    ├── paper1.pdf
    ├── paper2.pdf
    └── appendix1.pdf
```

如需添加论文链接，可以在论文标题中添加：
```html
<strong class="paper-title-bold">
    <a href="papers/paper1.pdf">论文标题</a>
</strong>
```

### 自定义颜色

编辑 `styles.css` 文件的第 10-18 行，修改颜色变量：

```css
:root {
    --primary-color: #1a1a1a;     /* 主要标题颜色 */
    --accent-color: #0066cc;      /* 强调色（链接、按钮） */
    --text-color: #333;           /* 正文颜色 */
    --sidebar-bg: #f9f9f9;        /* 侧边栏背景色 */
    ...
}
```

### 修改字体

在 `index.html` 的第 8 行，可以更换 Google Fonts：

```html
<link href="https://fonts.googleapis.com/css2?family=您喜欢的字体&display=swap" rel="stylesheet">
```

然后在 `styles.css` 第 23 行更新字体引用：
```css
font-family: '您的字体', Arial, sans-serif;
```

## 维护和更新

### 更新内容

1. 直接在 GitHub 网页上编辑文件，或
2. 克隆仓库到本地，修改后推送：

```bash
git clone https://github.com/username/username.github.io.git
cd username.github.io
# 编辑文件
git add .
git commit -m "更新内容"
git push
```

### 本地预览

在项目文件夹中打开 `index.html` 即可在浏览器中预览。

或者使用简单的 HTTP 服务器：

```bash
# Python 3
python -m http.server 8000

# 然后访问 http://localhost:8000
```

## 目录结构

```
your-repo/
├── index.html       # 主页面
├── styles.css       # 样式表
├── README.md        # 说明文档
├── cv/              # 简历文件夹（需要自己创建）
│   └── cv.pdf      # 简历 PDF
├── image/           # 图片文件夹（需要自己创建）
│   ├── profile.jpg  # 个人照片
│   ├── favicon-32x32.png    # 网站图标
│   ├── favicon-16x16.png
│   └── apple-touch-icon.png
└── papers/          # 论文文件夹（需要自己创建）
    ├── paper1.pdf
    └── paper2.pdf
```

## 功能特性

### 响应式设计
- 自动适配桌面、平板和手机屏幕
- 桌面端：左侧固定边栏 + 右侧主内容
- 移动端：上下堆叠布局

### 设计理念
- **极简主义**：减少视觉干扰，突出内容本身
- **学术专业**：参考顶级学者主页设计
- **易于维护**：纯 HTML + CSS，无需 JavaScript
- **主题分组**：按研究方向组织论文，而非按发表状态

## 技术栈

- HTML5
- CSS3（Grid 布局、CSS 变量、响应式设计）
- Google Fonts（可选）

## 浏览器兼容性

支持所有现代浏览器：
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+

## 常见问题

### 网站没有显示？

1. 检查仓库名是否为 `username.github.io`
2. 确认 GitHub Pages 已在设置中启用
3. 等待 5-10 分钟让 GitHub 构建网站

### 照片不显示？

1. 确保照片文件名为 `profile.jpg` 或 `profile.png`
2. 文件名大小写要匹配
3. 检查文件是否已成功上传

### 想要自定义域名？

在仓库设置的 GitHub Pages 部分，可以添加自定义域名。

## 参考资料

- [GitHub Pages 官方文档](https://docs.github.com/cn/pages)
- [Markdown 语法](https://guides.github.com/features/mastering-markdown/)
- [Git 基础教程](https://git-scm.com/book/zh/v2)

## 许可证

本模板可自由使用和修改，无需署名。

## 支持

如有问题或建议，欢迎提交 Issue。

---

**祝你拥有一个精美的学术主页！** 🎓

