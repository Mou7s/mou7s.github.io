# mou7s.github.io

这是一个极简静态站点仓库，唯一用途是将首页访问重定向到：

- `https://mou7s.com`

## 当前结构

```text
.
├─ index.html    # 纯静态跳转页
├─ README.md     # 仓库说明
├─ AGENTS.md     # 协作说明
└─ LICENSE       # 开源许可证
```

## 页面行为

`index.html` 同时使用了以下两种跳转方式：

- `meta refresh`
- `window.location.replace(...)`

这样在关闭 JavaScript 或某些缓存场景下也能尽量保持稳定跳转。

## 修改方式

如果只需要更换目标地址，直接编辑 `index.html` 中的目标链接即可，并确保以下位置保持一致：

- `meta refresh`
- `link rel="canonical"`
- 页面正文中的备用链接
- `window.location.replace(...)`

## 许可证

本项目采用 [MIT License](./LICENSE)。
