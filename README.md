# mou7s.github.io

基于 **Vite + Vue 3 + Tailwind CSS** 的静态站点项目。  
当前线上行为为首页自动跳转到：

- https://linktr.ee/mou7s

## 技术栈

- Vue 3
- Vite 5
- Tailwind CSS 3
- PostCSS + Autoprefixer

## 快速开始

建议使用 `pnpm`（仓库包含 `pnpm-lock.yaml`）：

```bash
pnpm install
pnpm dev
```

默认开发地址：`http://localhost:5173`

## 构建与预览

```bash
pnpm build
pnpm preview
```

- `pnpm build`：构建产物输出到 `dist/`
- `pnpm preview`：本地预览构建产物

## 项目结构

```text
.
├─ index.html              # 入口 HTML，包含跳转脚本
├─ src/
│  ├─ main.js              # Vue 应用入口
│  ├─ App.vue              # 根组件（当前为空）
│  └─ style.css            # Tailwind 样式入口
├─ tailwind.config.js      # Tailwind 配置
├─ postcss.config.js       # PostCSS 配置
└─ vite.config.js          # Vite 配置
```

## 当前页面行为

`index.html` 中包含以下跳转逻辑：

```html
<script>
  window.location.href = 'https://linktr.ee/mou7s';
</script>
```

如果要改为展示 Vue 页面，可移除该脚本并在 `src/App.vue` 中实现页面内容。

## 许可证

本项目使用 [MIT License](./LICENSE)。
