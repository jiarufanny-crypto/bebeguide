# Bébé Guide · 宝宝手册

法国0–6个月育儿助手 PWA — 中法双语待办清单 + 育儿知识库

## 部署到 Vercel（3分钟）

### 方法一：直接拖拽（最简单）

1. 打开 [vercel.com](https://vercel.com) 并登录（可用 GitHub 账号）
2. 点击 **Add New → Project**
3. 选择 **"Deploy without a Git repository"** → 拖拽整个 `bebe-guide` 文件夹上传
4. 点击 **Deploy** → 等待约30秒 → 获得网址 ✅

### 方法二：GitHub 自动部署（推荐，支持后续更新）

```bash
# 1. 初始化 git
cd bebe-guide
git init
git add .
git commit -m "init: Bébé Guide"

# 2. 在 GitHub 新建仓库，然后推送
git remote add origin https://github.com/你的用户名/bebe-guide.git
git push -u origin main
```

3. 回到 Vercel → **Add New → Project** → 选择刚创建的 GitHub 仓库
4. 点击 **Deploy** → 自动完成 ✅
5. 之后每次 `git push`，Vercel 自动重新部署

### 方法三：Vercel CLI

```bash
npm i -g vercel
cd bebe-guide
vercel --prod
```

## 添加到手机主屏幕（PWA）

部署成功后，用手机打开 Vercel 给你的网址：
- **iPhone**：Safari → 分享按钮 → 添加到主屏幕
- **Android**：Chrome → 菜单 → 添加到主屏幕

之后像原生 App 一样使用 🎉

## 文件结构

```
bebe-guide/
├── public/
│   └── index.html    ← 整个 App（单文件）
├── vercel.json       ← Vercel 配置
└── README.md
```
