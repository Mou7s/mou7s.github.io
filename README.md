# mou7s.github.io

一个基于 **Vite 5 + Vue 3 + Tailwind CSS 3** 的静态站点仓库。当前线上默认行为不是渲染页面，而是通过首页立即跳转到：

- `https://linktr.ee/mou7s`

如果后续需要恢复为真实站点页面，可以移除 `index.html` 中的跳转脚本，并在 `src/App.vue` 中实现内容。

## 技术栈

- Vue 3
- Vite 5
- Tailwind CSS 3
- PostCSS
- Autoprefixer

## 本地开发

推荐使用 `pnpm`，仓库已提交 `pnpm-lock.yaml`：

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

- `pnpm build`：生成生产构建，输出到 `dist/`
- `pnpm preview`：本地预览构建结果

提交前建议至少执行一次 `pnpm build`，确认没有导入错误、Vue 语法问题或 Tailwind 配置问题。

## 目录结构

```text
.
├─ index.html              # 入口 HTML，当前包含跳转逻辑
├─ public/                 # 静态资源目录
├─ src/
│  ├─ main.js              # Vue 应用入口
│  ├─ App.vue              # 根组件
│  └─ style.css            # Tailwind 样式入口
├─ vite.config.js          # Vite 配置
├─ tailwind.config.js      # Tailwind 配置
├─ postcss.config.js       # PostCSS 配置
└─ AGENTS.md               # 仓库协作说明
```

## 当前行为说明

首页跳转逻辑位于 `index.html`：

```html
<script>
  window.location.href = 'https://linktr.ee/mou7s';
</script>
```

这意味着即使 Vue 应用已挂载，生产环境访问首页时仍会优先跳转。若要恢复页面展示，需要先移除这段脚本。

## 许可证

本项目采用 [MIT License](./LICENSE)。
