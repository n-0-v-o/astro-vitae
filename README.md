# astro-vitae

基于 [Astro](https://astro.build/) 的单页个人主页，零额外依赖，计划部署至 GitHub Pages。

![页面预览](docs/preview.png)

## 功能

- **固定顶边栏**：毛玻璃效果，含 4 个板块导航（关于我 / 技能 / 项目 / 联系）
- **锚点快速定位**：点击导航项平滑滚动到对应板块，`scroll-padding-top` 避免标题被顶栏遮挡（零 JS）
- **滚动自动高亮**：基于 `IntersectionObserver`，页面滚动到某板块时顶栏对应导航项自动切换高亮

## 项目结构

```
src/pages/index.astro   # 单文件页面：板块数据、结构、样式、滚动高亮脚本
astro.config.mjs        # Astro 配置（部署 Pages 时需补 site/base）
docs/preview.png        # 页面预览图
```

板块由 `index.astro` 顶部的 `sections` 数组驱动，增删板块只需修改该数组。

## 本地运行

```sh
npm install
npm run dev      # 开发服务器 http://localhost:4321
npm run build    # 构建静态文件到 dist/
```

## 待办

- [ ] 替换各板块占位内容
- [ ] 部署到 GitHub Pages（配置 `site`/`base` + Actions 工作流）
