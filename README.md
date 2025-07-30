# XinC Blog

一个基于 VitePress 构建的个人博客，专注于分享技术笔记、工具推荐和日常记录。

## ✨ 特性

- 🎨 **现代化设计** - 简洁美观的界面设计，支持深色模式
- 📱 **响应式布局** - 完美适配桌面端和移动端
- 🔍 **全文搜索** - 集成 Algolia 搜索，快速查找内容
- 🏷️ **标签分类** - 支持文章标签和分类管理
- 📊 **访问统计** - 集成不蒜子访客统计
- 🎵 **音乐播放器** - 内置音乐组件，提升浏览体验
- 🖼️ **图片预览** - 支持图片放大预览功能
- 🚀 **动画效果** - 丰富的页面动画和交互效果

## 🛠️ 技术栈

- **框架**: VitePress
- **样式**: SCSS
- **动画**: GSAP
- **搜索**: Algolia
- **部署**: GitHub Pages
- **统计**: 不蒜子

## 📦 安装

```bash
# 克隆项目
git clone <your-repo-url>

# 进入项目目录
cd xinc-blog

# 安装依赖
npm install
```

## 🚀 开发

```bash
# 启动开发服务器
npm run docs:dev

# 构建生产版本
npm run docs:build

# 预览构建结果
npm run docs:preview
```

## 📁 项目结构

```
docs/
├── .vitepress/
│   ├── config.mts          # VitePress 配置
│   └── theme/              # 自定义主题
│       ├── components/     # 组件
│       ├── page/          # 页面组件
│       ├── style/         # 样式文件
│       └── utils/         # 工具函数
├── post/                  # 文章目录
│   └── blog/             # 博客文章
├── index.md              # 首页
├── archive.md            # 归档页面
├── tag.md               # 标签页面
└── tool.md              # 工具页面
```

## 📝 写作

在 `docs/post/` 目录下创建 Markdown 文件，支持以下 frontmatter：

```yaml
---
title: 文章标题
description: 文章描述
category: 分类名称
tags: 
  - 标签1
  - 标签2
---
```

## 🔧 配置

### Algolia 搜索

在 `docs/.vitepress/config.mts` 中配置 Algolia：

```typescript
algolia: {
  appId: 'your-app-id',
  apiKey: 'your-api-key',
  indexName: 'your-index-name'
}
```

### 部署配置

项目使用 GitHub Actions 自动部署，配置文件位于 `.github/workflows/deploy.yml`。

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！
