
## 说明

本仓库是 fork 自 [mpvue-loader](http://mpvue.com/build/mpvue-loader) 修改而来，主要为解决在页面文件中，`scoped` 的 `<style />` 中的 `page`、`body`、`html` 在页面中不生效的问题。

### 关于`mpvue` 对 `style` 的 `scoped` 的处理的结论

1. `vue.Component` 请一定添加 `scoped`，否则会污染引入处页面的样式。

2. `page` 中的样式加不加 `scoped`，都不会对其他内容造成影响，例如引入的组件。

3. `page` 中添加了 `scoped` 的样式，`html`、`page`、`body` 的样式转译后一定会失效。

如果需要统一团队无论是组件还是页面都需要添加 `scoped`，但是又需要 `page` 中 `scoped` 的样式生效，那你可能需要这个。
