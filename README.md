# 个人主页

一个使用 HTML、CSS 和 JavaScript 构建的轻量级个人主页，托管于 GitHub Pages。

## 目录结构

```
.
├── index.html          # 主页文件
├── css/
│   └── style.css       # 样式表
├── js/
│   └── main.js         # 交互脚本
├── assets/             # 静态资源（图片等）
└── README.md           # 说明文档
```

## 部署

推送到 GitHub 仓库后，在仓库 Settings > Pages 中选择 GitHub Actions 作为构建源，等待构建完成后访问 `https://你的用户名.github.io`。

## 自定义

- **个人信息**：在 `index.html` 中修改头像、名称和介绍
- **项目卡片**：复制 `project-card` 块添加新项目，修改图标、名称、描述和链接
- **主题颜色**：在 `css/style.css` 的 `:root` 中调整配色

## 许可证

MIT
