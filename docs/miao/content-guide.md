# 内容维护指南

这页回答两个最常见的问题：

- 我想在顶部导航栏新增一个栏目，应该怎么做？
- 我想在某个栏目里新增一篇文章，应该怎么做并上线？

## 基本规则

MkDocs 的内容都放在 `docs` 文件夹里：

```text
E:\Fun\Blog\notebook\
├─ mkdocs.yml
└─ docs\
   ├─ index.md
   └─ miao\
      ├─ index.md
      ├─ notebook-styles.md
      └─ content-guide.md
```

`docs` 里的 Markdown 文件是真正的文章；`mkdocs.yml` 里的 `nav` 决定它们如何显示在导航栏里。

## 新增一个顶部导航栏栏目

比如你想新增一个叫“课程”的栏目。

### 1. 新建文件夹和首页

在 `docs` 里新建：

```text
docs\courses\index.md
```

内容可以先写：

```markdown
# 课程

这里放课程笔记。
```

### 2. 修改 `mkdocs.yml`

找到：

```yaml
nav:
  - Home: index.md
  - 妙妙屋:
      - miao/index.md
```

改成：

```yaml
nav:
  - Home: index.md
  - 妙妙屋:
      - miao/index.md
      - Notebook 样式: miao/notebook-styles.md
      - 内容维护指南: miao/content-guide.md
      - 网站工作流: miao/website-workflow.md
  - 课程:
      - courses/index.md
```

这样顶部导航栏就会多出“课程”。

## 在某个栏目里新增文章

比如你想在“课程”下面新增一篇《线性代数第一章》。

### 1. 新建 Markdown 文件

路径：

```text
docs\courses\linear-algebra-ch1.md
```

内容：

```markdown
# 线性代数第一章

## 核心概念

- 向量
- 矩阵
- 线性变换
```

### 2. 把文章加入导航

在 `mkdocs.yml` 里：

```yaml
nav:
  - 课程:
      - courses/index.md
      - 线性代数第一章: courses/linear-algebra-ch1.md
```

保存后，这篇文章就会出现在“课程”栏目下。

## 只新增文章但不放进导航可以吗

可以。只要文件在 `docs` 里，它也会被构建，只是不出现在左侧/顶部导航中。

例如：

```text
docs\drafts\random-note.md
```

访问路径会类似：

```text
https://hgritty.github.io/notebook/drafts/random-note/
```

不过长期维护时，重要文章最好放进 `nav`，不然以后容易忘。

## 本地预览

每次改完内容，先本地预览：

```powershell
cd E:\Fun\Blog\notebook
mkdocs serve
```

打开：

```text
http://127.0.0.1:8000/
```

如果 8000 被占用：

```powershell
mkdocs serve -a 127.0.0.1:8001
```

## 部署上线

确认本地没问题后，执行：

```powershell
cd E:\Fun\Blog\notebook
git add .
git commit -m "update notebook"
git push
mkdocs gh-deploy
```

部署完成后访问：

```text
https://hgritty.github.io/notebook/
```

## 推荐命名习惯

文件夹和文件名建议用英文、小写、短横线：

```text
good:
docs\courses\linear-algebra.md
docs\tools\website-workflow.md

not recommended:
docs\课程\线性代数第一章.md
docs\My Notes\Chapter 1.md
```

这样链接更稳定，也更方便迁移。
