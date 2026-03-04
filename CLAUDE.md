# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目概述

伊朗战争新闻简报网站，基于 Astro 博客模板构建。发布关于美伊冲突的每日战况简报，内容为中文。

## 常用命令

```bash
npm run dev      # 启动开发服务器 (localhost:4321)
npm run build    # 构建生产版本到 ./dist/
npm run preview  # 预览构建结果
```

## 技术栈

- **Astro 5.x** - 静态站点生成器
- **TypeScript** (strict 模式)
- **MDX** - 支持 Markdown 中嵌入组件
- **Vercel Analytics** - 站点分析

## 架构

```
src/
├── content/blog/      # 博客文章 (Markdown/MDX)
├── components/        # Astro 组件
├── layouts/           # 页面布局模板
├── pages/             # 路由页面
└── styles/global.css  # 全局样式 (Bear Blog 风格)
```

## 内容管理

博客文章放在 `src/content/blog/`，使用 Content Collections 管理。

Frontmatter 必需字段：
```yaml
---
title: "文章标题"
description: "文章描述"
pubDate: "YYYY-MM-DD"
heroImage: "/path/to/image.jpg"  # 可选
---
```

## 站点配置

- `src/consts.ts` - 全局常量 (站点标题、描述)
- `astro.config.mjs` - Astro 配置
- `src/content.config.ts` - 内容集合 schema 定义
