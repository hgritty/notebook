# 网站工作流

目前三个网站项目是独立的：

```text
E:\Fun\Blog\
├─ hgritty\     # Hexo 博客
├─ notebook\    # MkDocs 知识库
└─ game2048\    # 独立小游戏
```

## 互相影响吗

不影响。它们是三个独立仓库、三套发布流程，只是都挂在同一个 GitHub Pages 域名下面：

| 项目 | 地址 | 说明 |
| --- | --- | --- |
| hgritty | `https://hgritty.github.io/` | Hexo + Butterfly 博客 |
| notebook | `https://hgritty.github.io/notebook/` | MkDocs Material 知识库 |
| game2048 | `https://hgritty.github.io/game2048/` | 独立静态小游戏 |

## 更新 notebook

```powershell
cd E:\Fun\Blog\notebook
mkdocs serve
```

写完后：

```powershell
git add .
git commit -m "update notebook"
git push
mkdocs gh-deploy
```

## 更新 Hexo 博客

```powershell
cd E:\Fun\Blog\hgritty
hexo clean
hexo g
hexo d
```

## 更新 game2048

```powershell
cd E:\Fun\Blog\game2048
git add .
git commit -m "update game2048"
git push
```
