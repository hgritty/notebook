# Website Workflow

## Local Projects

```text
E:\Fun\Blog\
├─ hgritty\     # Hexo blog
├─ notebook\    # MkDocs knowledge base
└─ game2048\    # standalone static game
```

## Notebook

```powershell
cd E:\Fun\Blog\notebook
mkdocs serve
mkdocs gh-deploy
```

## Hexo Blog

```powershell
cd E:\Fun\Blog\hgritty
hexo clean
hexo g
hexo d
```
