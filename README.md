# Wolffy1998 - 个人主页

这是一个为 GitHub Pages 构建的个人主页网站，部署在 [wolffy1998.github.io](https://wolffy1998.github.io)。

## 目录结构

```
.
├── index.html              # 主页文件（所有页面内容都在这个文件里）
├── css/
│   └── style.css           # 样式表（颜色、布局、动画）
├── js/
│   └── main.js             # JavaScript（移动端导航交互）
├── .github/
│   └── workflows/
│       └── deploy.yml      # GitHub Actions 自动部署配置
├── .nojekyll               # 告诉 GitHub Pages 跳过 Jekyll 处理
└── README.md               # 本说明文档
```

---

## 部署方式

### 第一步：推送到 GitHub

将此文件夹中的所有文件推送到你的 GitHub 仓库 `wolffy1998/wolffy1998.github.io` 的 `main` 分支：

```bash
cd "此项目文件夹"
git init
git add .
git commit -m "初始化个人主页"
git remote add origin https://github.com/wolffy1998/wolffy1998.github.io.git
git branch -M main
git push -u origin main
```

### 第二步：配置 GitHub Pages

1. 打开你的仓库页面：`https://github.com/wolffy1998/wolffy1998.github.io`
2. 点击 **Settings（设置）** > **Pages（页面）**
3. 在 **Build and deployment** 部分：
   - **Source** 选择：**GitHub Actions**
4. 等待 GitHub Actions 自动构建完成（约 1-2 分钟）
5. 访问 `https://wolffy1998.github.io` 即可查看你的主页

---

## 自定义修改指南

所有内容都在 `index.html` 文件中修改。用任何文本编辑器（如 VS Code、Notepad++）打开即可编辑。

### 一、修改头像

找到这行代码（在首页 `hero` 区域）：

```html
<img src="https://avatars.githubusercontent.com/u/placeholder?v=4" alt="Wolffy1998 头像">
```

**修改方法：**
- 将 `src` 的值替换为你的头像图片链接
- 可以直接使用你的 GitHub 头像：`https://avatars.githubusercontent.com/u/你的GitHub用户名?v=4`
- 也可以上传一张图片到你的仓库，然后用相对路径引用

### 二、修改个人介绍（首页区域）

找到并修改以下内容：

| 要修改的内容 | 在代码中的位置 | 说明 |
|-------------|---------------|------|
| 你的昵称 | `<h1 class="hero-title">` 里的名字 | 页面正中央显示的名字 |
| 副标题 | `<p class="hero-subtitle">` | 名字下方的身份描述 |
| 个人简介 | `<p class="hero-description">` | 首页的简短介绍文字 |

### 三、修改社交媒体链接（首页底部图标）

找到 `<div class="hero-socials">` 部分：

```html
<div class="hero-socials">
  <a href="https://github.com/wolffy1998" target="_blank" rel="noopener" aria-label="GitHub">
    <i class="fab fa-github"></i>
  </a>
  <!-- 更多链接... -->
</div>
```

**修改方法：**
- 将 `href` 替换为你的真实社交主页链接
- 删除不需要的 `<a>` 标签即可移除图标
- 添加新图标：复制一个 `<a>` 标签并修改

### 四、修改项目展示

找到 `<div class="projects-grid">` 部分，里面包含多个 `<div class="project-card">`。

#### 修改单个项目卡片

每个项目卡片包含：

```html
<div class="project-card">
  <div class="project-icon">
    <i class="fas fa-code"></i>           <!-- 项目图标 -->
  </div>
  <h3 class="project-title">项目 Alpha</h3>  <!-- 项目名称 -->
  <p class="project-description">          <!-- 项目描述 -->
    在这里简要描述你的第一个项目...
  </p>
  <div class="project-tags">
    <span class="tag">Python</span>        <!-- 技术标签 -->
    <span class="tag">Web</span>
  </div>
  <div class="project-links">
    <a href="https://github.com/...">      <!-- GitHub 链接 -->
      <i class="fab fa-github"></i> 源代码
    </a>
  </div>
</div>
```

**修改指南：**

1. **图标**：替换 `<i class="fas fa-xxx">` 中的图标名称
   - 可用图标列表：[Font Awesome 图标库](https://fontawesome.com/icons)
   - 常用图标：`fa-code`、`fa-mobile-alt`、`fa-robot`、`fa-terminal`、`fa-gamepad`、`fa-database`、`fa-cloud`、`fa-paint-brush`

2. **项目名称**：修改 `<h3 class="project-title">` 内的文字

3. **项目描述**：修改 `<p class="project-description">` 内的文字

4. **技术标签**：修改 `<span class="tag">` 内的文字，可以增加或删除标签

5. **链接**：修改 `href` 为真实的 GitHub 仓库链接或演示链接

#### 添加新项目

复制一个完整的 `<div class="project-card">...</div>` 粘贴到 `<div class="projects-grid">` 内部即可。

#### 删除项目

删除对应的 `<div class="project-card">...</div>` 整块代码。

### 五、修改"关于我"区域

找到 `<section id="about">` 部分：

```html
<section id="about" class="about">
  ...
  <div class="about-text">
    <p>你好！我是 <strong>Wolffy1998</strong>...</p>  <!-- 修改自我介绍 -->
    <p>我相信开源和社区的力量...</p>              <!-- 修改第二段介绍 -->

    <div class="about-stats">
      <div class="stat">
        <span class="stat-number">4+</span>         <!-- 修改数字 -->
        <span class="stat-label">项目</span>         <!-- 修改标签名 -->
      </div>
      <!-- 更多统计数据... -->
    </div>
  </div>
</section>
```

**修改指南：**
- 修改 `<p>` 标签内的自我介绍文字
- 修改 `stat-number` 里的数字和 `stat-label` 里的文字
- 增加/删除 `<div class="stat">` 块来调整统计项数量

### 六、修改联系方式

找到 `<section id="contact">` 部分，里面包含多个 `<a class="contact-card">`：

```html
<div class="contact-grid">
  <a href="mailto:wolffy1998@example.com" class="contact-card">
    <div class="contact-icon">
      <i class="fas fa-envelope"></i>       <!-- 联系方式图标 -->
    </div>
    <h3>邮箱</h3>                            <!-- 标题 -->
    <p>wolffy1998@example.com</p>            <!-- 显示的联系信息 -->
  </a>
  <!-- 更多联系卡片... -->
</div>
```

**修改指南：**

1. **邮箱**：将 `href="mailto:xxx"` 和 `<p>` 标签内的邮箱地址都替换为你的真实邮箱
2. **GitHub**：将 `href` 替换为你的 GitHub 主页
3. **Twitter/X**：将 `href` 替换为你的 Twitter 主页
4. **Discord**：将 `href` 替换为你的 Discord 邀请链接
5. **添加新联系方式**：复制一个 `<a>` 块并修改内容
6. **删除联系方式**：删除对应的 `<a>` 块

**常用联系方式图标：**
| 平台 | 图标类名 |
|------|---------|
| 邮箱 | `fas fa-envelope` |
| GitHub | `fab fa-github` |
| Twitter/X | `fab fa-x-twitter` |
| Discord | `fab fa-discord` |
| 微信 | `fab fa-weixin` |
| QQ | `fab fa-qq` |
| 微博 | `fab fa-weibo` |
| Bilibili | `fab fa-bilibili` |
| 知乎 | 可用 `fas fa-comment-dots` 代替 |
| Telegram | `fab fa-telegram` |

### 七、修改页脚

找到 `<footer>` 部分：

```html
<footer class="footer">
  <div class="container">
    <p>&copy; 2024-2026 Wolffy1998. 用 <i class="fas fa-heart"></i> 构建...</p>
  </div>
</footer>
```

修改年份和名字即可。

---

## 进阶自定义（可选）

### 修改主题颜色

打开 `css/style.css`，在文件最上方找到 `:root` 部分：

```css
:root {
  --primary: #6366f1;          /* 主色调（紫色） */
  --primary-dark: #4f46e5;     /* 主色调深色 */
  --primary-light: #818cf8;    /* 主色调浅色 */
  --bg-dark: #0f172a;          /* 页面背景色 */
  --bg-card: #1e293b;          /* 卡片背景色 */
  ...
}
```

修改这些颜色值即可改变整个网站的主题色。

### 修改字体

`index.html` 中使用了 Google Fonts 的 **Noto Sans SC**（思源黑体），支持中文显示。如需更换字体，修改 `<head>` 中的 `<link>` 标签和 `style.css` 中的 `font-family`。

---

## 常见问题

### Q: 修改后如何更新到网站？

只需将修改后的文件 `git push` 到仓库的 `main` 分支，GitHub Actions 会自动重新部署。

### Q: 网站没有更新怎么办？

1. 确认文件已经成功推送到 GitHub
2. 检查 GitHub Actions 是否运行成功（仓库 Actions 标签页）
3. 浏览器强制刷新：`Ctrl + Shift + R`（Windows）或 `Cmd + Shift + R`（Mac）
4. 清除浏览器缓存后重试

### Q: 如何预览修改效果？

直接用浏览器打开 `index.html` 文件即可在本地预览，不需要本地服务器。

### Q: 404 错误怎么办？

确认仓库名称是 `wolffy1998.github.io`，且 Settings > Pages 中已选择 **GitHub Actions** 作为构建源。

---

## 许可证

MIT
