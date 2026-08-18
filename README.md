# Personal Homepage · 个人主页

一个基于 **GitHub Pages** 的静态个人主页，介绍自己、展示部署的项目和联系方式。

> 🌐 线上地址：<https://wolffy1998.github.io>
> 📦 仓库：`wolffy1998/wolffy1998.github.io`（用户主页仓库，部署在根路径）

页面内容全部由根目录的 **`config.yml`** 驱动 —— 修改配置即可更新页面，**无需改动任何代码**。

## 📁 项目结构

```
wolffy1998.github.io/
├── index.html    # 页面（读取 config.yml 渲染，一般不用动）
├── config.yml    # ⭐ 所有内容配置：个人信息 / 项目 / 联系方式 / 图标 / 头像文件名
├── avatar.jpg    # 头像图片（文件名在 config.yml 的 profile.avatar 中定义）
├── .nojekyll     # 禁用 Jekyll 处理，文件原样发布
└── README.md     # 本文档
```

## 🚀 快速开始

### 1. 修改配置

编辑 `config.yml`，把示例内容替换成你自己的信息：

| 配置段 | 作用 |
|---|---|
| `site` | 站点标题、标语、页脚、主题色 `accent` |
| `profile` | 姓名、头像、职位、简介、所在地、技能标签 |
| `projects` | 项目列表：名称、简介、在线地址、仓库、图标、标签 |
| `contacts` | 联系方式：邮箱、GitHub、微信、B 站等 |

### 2. 头像（可选）

头像文件放在**项目根目录**，文件名和后缀在 `config.yml` 中定义，二者保持一致即可：

```yaml
profile:
  avatar: "avatar.jpg"    # 默认名 avatar.jpg，改成 avatar.png / avatar.webp 等都行
```

也支持直接填在线图片 URL（`https://...`）。不配置头像时会自动显示姓名首字作为默认头像；配置的图片加载失败时同样会回退显示首字。

### 3. 图标说明

页面所有图标来自 **[Font Awesome 6](https://fontawesome.com/search)**（免费版，通过 cdnjs CDN 引入，无需安装任何东西）。

**如何找到想要的图标：**

1. 打开 <https://fontawesome.com/search>；
2. 搜索关键词（英文），如 `github`、`wechat`、`bilibili`、`envelope`、`gamepad`；
3. 点进图标详情页，复制它的类名（Class），格式为 `样式前缀 + 图标名`；
4. 把类名填到 `config.yml` 的 `icon` 字段即可。

**三种常用前缀：**

| 前缀 | 含义 | 示例 |
|---|---|---|
| `fa-brands` | 品牌 Logo（GitHub、微信、B 站、知乎…） | `fa-brands fa-github` |
| `fa-solid` | 实心通用图标（邮箱、火箭、游戏手柄…） | `fa-solid fa-envelope` |
| `fa-regular` | 线性通用图标 | `fa-regular fa-heart` |

```yaml
# 项目图标
- name: "个人主页"
  icon: "fa-solid fa-house"

# 联系方式图标
- label: "GitHub"
  icon: "fa-brands fa-github"
```

> 💡 也支持直接写 emoji（如 `icon: "🚀"`），页面会原样显示，适合不想查图标类名的场景。

## 💻 本地预览

> ⚠️ 不能直接双击 `index.html` 打开 —— `file://` 协议下浏览器禁止读取本地 `config.yml`，页面会提示加载失败。

在项目目录下任选一种方式启动本地服务器：

```bash
# Python
python -m http.server 8000

# Node.js
npx serve .
```

然后浏览器访问 <http://localhost:8000> 即可预览。

## 🌐 部署到 GitHub Pages

1. 在 GitHub 上新建一个仓库（例如 `yourname.github.io` 或任意名字）；
2. 把本项目所有文件推送到仓库：

   ```bash
   git init
   git add .
   git commit -m "init: personal homepage"
   git branch -M main
   git remote add origin https://github.com/<你的用户名>/<仓库名>.git
   git push -u origin main
   ```

3. 打开仓库 **Settings → Pages**：
   - Source 选择 `Deploy from a branch`
   - Branch 选择 `main` / `/ (root)`，点 Save；
4. 等待 1~2 分钟，访问 `https://<你的用户名>.github.io/<仓库名>/` 即可。

> 💡 如果仓库恰好叫 `<用户名>.github.io`，则直接通过 `https://<用户名>.github.io` 访问。

## ✏️ 之后如何更新内容

改 `config.yml` → 提交推送：

```bash
git add config.yml
git commit -m "update: 修改个人信息"
git push
```

GitHub Pages 会在一分钟内自动重新部署，页面内容随之更新。

## 📄 License

MIT
