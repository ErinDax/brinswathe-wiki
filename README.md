# brinswathe-wiki

Brin's Wathe（b-w）模组 Wiki —— MkDocs Material + GitHub Pages 自动部署。

## 本地预览（可选，需 Python）

```bash
pip install mkdocs-material
mkdocs serve
```

## 部署（GitHub Pages 自动）

1. 把本项目 push 到 GitHub 仓库（如 `brinswathe-wiki`）
2. 仓库 Settings → Pages → Source 选 **GitHub Actions**
3. push 到 `main` 分支后自动构建部署

## 目录

- `docs/` — 全部 wiki 内容（markdown）
- `mkdocs.yml` — 站点配置（改 nav 加页面）
- `.github/workflows/ci.yml` — 自动构建部署

> 记得把 `mkdocs.yml` 里的 `YOUR_USERNAME` 改成你的 GitHub 用户名。
