# Yuji's Blog

这是一个基于 Hugo 框架的个人博客网站，主要用于分享 AI 探索相关的内容。

## 特点

- 使用 Hugo 框架构建
- 采用 Stack 主题
- 支持文章搜索功能
  - 标题、内容搜索
  - 标签、分类搜索
  - 实时搜索结果
  - 高亮匹配文本
- 响应式设计
- 支持 Markdown 写作
- 自动部署到 GitHub Pages

## 本地开发

1. 安装 Hugo
```bash
brew install hugo
```

2. 克隆仓库
```bash
git clone https://github.com/xuyuji/xuyuji.github.io.git
cd xuyuji.github.io
```

3. 启动本地服务器
```bash
hugo server -D
```

访问 http://localhost:1313 查看效果

## 部署

本站使用 GitHub Pages 部署，访问地址：https://xuyuji.github.io

- 提交到 main 分支会自动触发部署
- 部署过程由 GitHub Actions 自动完成
- 部署完成后约 1-2 分钟生效

## 功能说明

### 搜索功能

1. 访问搜索页面：https://xuyuji.github.io/search/
2. 在搜索框中输入关键词
3. 实时显示匹配的文章
4. 支持以下搜索范围：
   - 文章标题
   - 文章内容
   - 文章标签
   - 文章分类

### 文章发布

请参考 [文章发布指南](docs/POST_GUIDE.md) 了解如何发布新文章。

## 许可证

MIT License