# Notebook 样式

这一页专门放在 notebook 里可复用的写法。以后忘了怎么写，就来这里抄。

## 加粗和强调

```markdown
**重要内容**
*轻微强调*
==高亮文字==
~~删除线~~
```

效果：

**重要内容**

*轻微强调*

==高亮文字==

~~删除线~~

## 提示框

```markdown
!!! note "普通提示"
    适合放补充说明。

!!! tip "技巧"
    适合放经验、窍门、推荐做法。

!!! warning "注意"
    适合放容易踩坑的点。

!!! danger "危险"
    适合放会造成严重后果的操作。
```

效果：

!!! note "普通提示"
    适合放补充说明。

!!! tip "技巧"
    适合放经验、窍门、推荐做法。

!!! warning "注意"
    适合放容易踩坑的点。

!!! danger "危险"
    适合放会造成严重后果的操作。

## 可折叠内容

```markdown
??? question "点开查看答案"
    这里是折叠起来的内容。
```

效果：

??? question "点开查看答案"
    这里是折叠起来的内容。

## 自定义加粗框

```html
<div class="note-box">
  <strong>重点：</strong>
  这里可以放一段特别想凸显的话。
</div>
```

效果：

<div class="note-box">
  <strong>重点：</strong>
  这里可以放一段特别想凸显的话。
</div>

## 任务列表

```markdown
- [x] 建好 notebook
- [x] 部署到 GitHub Pages
- [ ] 慢慢填内容
```

效果：

- [x] 建好 notebook
- [x] 部署到 GitHub Pages
- [ ] 慢慢填内容

## 表格

```markdown
| 类型 | 用途 |
| --- | --- |
| Blog | 时间流记录 |
| Notebook | 长期知识整理 |
```

效果：

| 类型 | 用途 |
| --- | --- |
| Blog | 时间流记录 |
| Notebook | 长期知识整理 |

## 代码块

````markdown
```powershell
cd E:\Fun\Blog\notebook
mkdocs serve
```
````

效果：

```powershell
cd E:\Fun\Blog\notebook
mkdocs serve
```

## 数学公式

```markdown
行内公式：\( E = mc^2 \)

块级公式：

\[
\sum_{i=1}^{n} i = \frac{n(n+1)}{2}
\]
```

效果：

行内公式：\( E = mc^2 \)

\[
\sum_{i=1}^{n} i = \frac{n(n+1)}{2}
\]

## 键盘按键

```markdown
++ctrl+c+++ 复制
++ctrl+v+++ 粘贴
```

效果：

++ctrl+c+++ 复制

++ctrl+v+++ 粘贴
