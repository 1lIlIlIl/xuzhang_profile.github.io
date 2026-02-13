# 快速开始指南 | Quick Start Guide

## 🚀 5分钟快速部署

### 第一步：初始化 Git 仓库

```powershell
cd c:\Users\31588\Desktop\Profile
git init
git config user.name "Zhang Xu"
git config user.email "mail_zhangxu@126.com"
```

### 第二步：创建 GitHub 仓库

1. 访问 [github.com/new](https://github.com/new)
2. 仓库名：`yourusername.github.io`（用你的GitHub用户名替换）
3. 选择 **Public**
4. 创建仓库

### 第三步：推送到 GitHub

```powershell
git add .
git commit -m "Initial portfolio site"
git branch -M main
git remote add origin https://github.com/yourusername/yourusername.github.io.git
git push -u origin main
```

稍等2-5分钟，你的网站将在以下位置上线：
**https://yourusername.github.io**

---

## 📋 项目内容清单

### 核心文件
- ✅ [index.html](index.html) — 主网页（包含所有内容）
- ✅ [css/style.css](css/style.css) — 完整样式系统（~800行）
- ✅ [js/script.js](js/script.js) — 交互与动画

### 文档
- ✅ [README.md](README.md) — 项目介绍
- ✅ [DEPLOYMENT.md](DEPLOYMENT.md) — 部署指南
- ✅ [STYLE_GUIDE.md](STYLE_GUIDE.md) — 设计系统
- ✅ [QUICK_START.md](QUICK_START.md) — 本文件

### 配置
- ✅ [package.json](package.json) — 项目元数据
- ✅ [.gitignore](.gitignore) — Git 忽略文件
- ✅ [.github/workflows/deploy.yml](.github/workflows/deploy.yml) — 自动部署

---

## 🎨 设计风格说明

你的网站融合了三位设计大师的理念：

### 1️⃣ **Virgil Abloh** (建筑感)
- 明确的几何形状与边框
- 大胆的排版和数字标号
- 战略性的留白
- 网格化布局

### 2️⃣ **Matthew Williams** (精致感)
- 精确的测量和细节
- 分层的信息架构
- 极简主义手法
- 结构化的设计

### 3️⃣ **Maison Margiela** (解构感)
- 解构式的视觉元素
- 边框和分割线
- 不对称的构图
- 隐喻的奢华

---

## 🔧 本地预览

### 方法1：直接打开（最简单）
```powershell
Invoke-Item "c:\Users\31588\Desktop\Profile\index.html"
```

### 方法2：使用 Python 本地服务器
```powershell
cd c:\Users\31588\Desktop\Profile
python -m http.server 8000
# 然后访问 http://localhost:8000
```

### 方法3：使用 Node.js
```powershell
npm install -g http-server
cd c:\Users\31588\Desktop\Profile
http-server
```

---

## ✏️ 个性化编辑

### 修改GitHub链接
在 `index.html` 的联系部分，替换：
```html
<a href="https://github.com/yourusername" class="contact-link" target="_blank">
```

### 更新LinkedIn链接
```html
<a href="https://linkedin.com/in/yourusername" class="contact-link" target="_blank">
```

### 更改配色方案
编辑 `css/style.css` 的 `:root` 部分：
```css
:root {
    --color-primary: #000000;      /* 主色 */
    --color-secondary: #ffffff;    /* 背景 */
    --color-accent: #888888;       /* 辅助色 */
}
```

---

## 📱 响应式测试

网站支持：
- ✓ 桌面版 (1200px+)
- ✓ 平板版 (768px - 1199px)
- ✓ 手机版 (320px - 767px)

**在浏览器中测试：**
```
F12 → Toggle Device Toolbar → 选择不同设备
```

---

## 🌐 自定义域名 (可选)

### 如果你有自己的域名

1. **编辑 CNAME 文件**
   在项目根目录创建 `CNAME` 文件：
   ```
   yourdomain.com
   ```

2. **配置 DNS**
   - A 记录: 指向 GitHub IPs
   - 或 CNAME 记录: 指向 `yourusername.github.io`

3. **GitHub 设置**
   - Repository Settings → Pages
   - Custom domain: `yourdomain.com`
   - 启用 HTTPS

---

## 🔍 SEO 优化建议

编辑 `index.html` 的 `<head>` 部分，添加：

```html
<meta name="description" content="Zhang Xu - Flexible Electronics & Neuromorphic Computing Researcher">
<meta name="keywords" content="flexible electronics, neuromorphic computing, wearables, research">
<meta property="og:title" content="Zhang Xu | Research Portfolio">
<meta property="og:type" content="website">
```

---

## 🚀 后续更新

每次更新网站：

```powershell
# 1. 编辑文件
# 2. 提交更改
git add .
git commit -m "描述你的更改"
git push origin main
```

GitHub Pages 会自动重新部署（2-5分钟内生效）。

---

## 📊 文件结构详解

```
Profile/
├── index.html                    ← 所有内容在这里
├── css/
│   └── style.css               ← 完整设计系统
├── js/
│   └── script.js               ← 交互和动画
├── assets/                      ← (预留用于图片)
├── .github/
│   └── workflows/
│       └── deploy.yml          ← 自动部署配置
├── README.md                   ← 项目说明
├── DEPLOYMENT.md               ← 详细部署指南
├── STYLE_GUIDE.md              ← 设计系统文档
├── QUICK_START.md              ← 本文
├── package.json                ← 项目元数据
├── .gitconfig                  ← Git 配置
└── .gitignore                  ← Git 忽略规则
```

---

## 🆘 常见问题

**Q: 网站不显示？**
A: 
- 确认仓库名为 `yourusername.github.io`
- 确认仓库是 public
- 等待 2-5 分钟
- 清除浏览器缓存 (Ctrl+Shift+Delete)

**Q: 自定义域名不工作？**
A: 
- 检查 CNAME 文件是否正确
- DNS 设置需要 24-48 小时生效
- 在 Repository Settings 中启用 HTTPS

**Q: 如何添加新的项目？**
A: 编辑 `index.html`，复制 `.project-item` div 并修改内容

**Q: 可以添加博客功能吗？**
A: 可以，需要使用 Jekyll 或其他静态生成器。推荐使用 Hugo 或 Next.js

---

## 📚 有用的资源

- [GitHub Pages 官方文档](https://docs.github.com/en/pages)
- [HTML 参考](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [CSS 参考](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [Web 设计最佳实践](https://www.w3.org/WAI/)

---

## ✨ 设计亮点

### 1. 几何动画
- 悬浮的几何形状在 Hero 部分
- 光滑的滚动动画
- 细微的视差效果

### 2. 排版系统
- Playfair Display：优雅的展示
- Montserrat：现代的正文
- 精确的字距调整

### 3. 交互设计
- 按钮悬停效果
- 卡片提升动画
- 平滑的导航过渡

### 4. 响应式布局
- 移动优先方法
- 灵活的网格系统
- 自适应排版

---

## 🎯 下一步行动

1. ✅ 初始化 Git 仓库
2. ✅ 创建 GitHub 仓库
3. ✅ 推送代码
4. ✅ 访问 `yourusername.github.io`
5. ✅ 更新 GitHub/LinkedIn 链接
6. ✅ （可选）设置自定义域名
7. ✅ 分享你的作品集！

---

**祝贺！** 你现在拥有一个专业的研究者个人主页。 🎉

有任何问题，联系：mail_zhangxu@126.com
