# YvonneHuang 的编程笔记

> 一个编程零基础选手的 C 语言踩坑实录。

这不是教程站。这里记的每一篇，都是我自己在 OJ 做题时真实卡住过、并且最后搞明白的错误。

## 在线访问

GitHub Pages 地址：发布后填在这里（`https://<你的用户名>.github.io/<仓库名>/`）

## 里面有什么

| 文章 | 踩的坑 |
| --- | --- |
| [改了代码，为什么运行结果没变？](posts/01-edit-compile-run.html) | 编辑 / 编译 / 运行是三件独立的事 |
| [scanf 里那个 &，到底是什么东西？](posts/02-scanf-ampersand.html) | 少写 `&` 导致运行时崩溃（SIGTRAP） |
| [1 除以 2 居然等于 0](posts/03-integer-division.html) | C 语言整数除法直接截断小数 |
| [一个空格引发的「答案错误」](posts/04-output-format.html) | OJ 逐字符比对，多余空格也算错 |
| [报错指向的那一行，不一定是出错的那一行](posts/05-error-line.html) | 函数定义末尾多写分号 |

每篇都按 **现象 → 我的猜想 → 动手验证 → 真正的原因 → 记住什么** 的顺序写。

## 项目结构

```
my-blog/
├── index.html          首页：介绍 + 文章列表
├── about.html          关于页
├── posts/              文章页（每篇一个 HTML 文件）
│   ├── 01-edit-compile-run.html
│   ├── 02-scanf-ampersand.html
│   ├── 03-integer-division.html
│   ├── 04-output-format.html
│   └── 05-error-line.html
└── assets/
    └── style.css       全站样式
```

## 怎么在本地看

不需要装任何东西。直接双击 `index.html`，用浏览器打开就能看。

如果想用本地服务器预览（更接近线上效果），在项目目录里执行：

```bash
python -m http.server 8000
```

然后浏览器访问 `http://localhost:8000`。

## 技术说明

- **纯静态网站**，手写 HTML + CSS，零依赖、零构建步骤。
- 没有使用博客框架或生成器——作为初学者，我不想让配环境挡在「把文章发出去」前面。
- 响应式布局，手机上也能正常阅读。
- 部署方式：GitHub Pages。

## 关于 AI 的使用

文章内容是我在学习过程中真实遇到的经历；AI 助手帮助我把这些经历整理成文、排版成网页、并生成了全站的代码与样式。

## 后续想做的

- [ ] 继续更新刷题踩坑记录
- [ ] 加上代码高亮
- [ ] 加一个简单的文章分类 / 标签页
