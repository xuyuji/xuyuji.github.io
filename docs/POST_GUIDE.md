# 文章发布指南

本文档详细说明如何在博客上发布新文章。

## 文章创建流程

### 1. 创建文章文件

在 `content/posts` 目录下创建新的 Markdown 文件，文件名格式建议：`YYYY-MM-DD-title.md`

例如：`2024-02-18-ai-introduction.md`

### 2. 文章头部信息

每篇文章都需要包含以下头部信息：

```markdown
---
title: "文章标题"
description: "文章描述"
date: YYYY-MM-DD
image: "/img/your-image.jpg"  # 可选
categories:
    - 分类1
    - 分类2
tags:
    - 标签1
    - 标签2
draft: false  # 设置为 true 则为草稿
---
```

注意：
- `categories` 和 `tags` 会被用于文章分类和搜索
- `description` 会显示在搜索结果中
- `draft: true` 的文章只在本地开发时可见

### 3. 图片添加

1. 将图片文件放在 `static/img/posts` 目录下
2. 在文章中引用图片：`![图片描述](/img/posts/your-image.jpg)`

### 4. 本地预览

1. 启动本地服务器：
```bash
hugo server -D
```

2. 访问 http://localhost:1313 预览效果
3. 可以通过搜索功能验证文章是否可被检索到

### 5. 发布文章

1. 确认文章无误后，提交到 Git：
```bash
git add .
git commit -m "Add new post: 文章标题"
git push origin main
```

2. 等待 GitHub Actions 自动部署（约1-2分钟）
3. 访问 https://yuji-blog.github.io 查看效果

## 文章编写建议

### 1. 文章结构
- 清晰的标题层级
- 适当的段落分隔
- 使用列表和表格组织内容
- 添加相关图片和代码示例

### 2. Markdown 语法
- 使用 `#` 创建标题（H1-H6）
- 使用 `*` 或 `_` 实现斜体和粗体
- 使用 ``` 创建代码块，并指定语言
- 使用 `>` 创建引用
- 使用 `---` 创建分隔线

### 3. SEO 优化
- 使用有意义的文件名
- 填写合适的描述（description）
- 选择准确的分类和标签
- 为图片添加 alt 文本

### 4. 搜索优化
- 使用清晰的文章标题
- 添加合适的文章描述
- 选择相关的标签和分类
- 在文章开头提供摘要

## 常见问题

### 1. 图片不显示
- 检查图片路径是否正确
- 确认图片已放入 `static/img/posts` 目录
- 检查图片格式是否支持（推荐使用 jpg, png）

### 2. 预览不更新
- 检查本地服务器是否运行
- 尝试重启 hugo server
- 清除浏览器缓存

### 3. 部署失败
- 检查 Git 提交是否成功
- 查看 GitHub Actions 运行状态
- 确认文章格式是否正确

### 4. 搜索问题
- 确认文章不是草稿状态
- 检查标签和分类是否正确设置
- 等待部署完成后再测试搜索

## 小贴士

1. 使用 VS Code 等编辑器，安装 Markdown 预览插件
2. 定期备份文章源文件
3. 遵循一致的命名规范
4. 保持文章分类和标签的统一性
5. 定期更新和维护文章内容
6. 使用搜索功能检查文章是否重复

## 参考资源

- [Hugo 文档](https://gohugo.io/documentation/)
- [Markdown 基础语法](https://www.markdownguide.org/basic-syntax/)
- [Stack 主题文档](https://stack.jimmycai.com/) 