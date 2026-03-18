# Claw 导航站（独立版）

这是一个纯静态导航站，不依赖 `openclaw101` 模板。

## GitHub Pages 发布

仓库推送到 `main` 后会自动触发部署：

- 工作流文件：`.github/workflows/deploy-pages.yml`
- 预计访问地址：`https://guoxinling.github.io/clawtab/`

首次发布时，需要在 GitHub 仓库里确认一次：

1. 打开仓库 `Settings > Pages`
2. `Build and deployment` 选择 `Source: GitHub Actions`
3. 等待 `Actions` 页里的 `Deploy to GitHub Pages` 变成绿色

## 本地打开

方式 1：直接双击 `index.html`。

方式 2：起本地静态服务（推荐）：

```bash
cd /Users/guoxl/Documents/Playground/claw-nav-site
python3 -m http.server 5173
```

浏览器访问：

- http://localhost:5173

## 文件结构

- `index.html`: 页面结构
- `styles.css`: 视觉与响应式样式
- `app.js`: 数据、筛选、搜索、渲染逻辑
- `.github/workflows/deploy-pages.yml`: Pages 自动部署
- `.nojekyll`: 禁用 Jekyll 处理

## 如何加链接

在 `app.js` 的 `resources` 数组中新增对象：

- `title`
- `desc`
- `url`
- `source`
- `lang` (`zh` / `en`)
- `category`
- `featured` (`true` / `false`)
- `tags`
