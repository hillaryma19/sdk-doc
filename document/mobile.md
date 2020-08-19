# 文档移动端插件

加载此插件可以使文档适配移动端网页。

## 构造函数

-   用法

```js
const Editor = shimo.sdk.document.Editor
const Mobile = shimo.sdk.document.plugins.Mobile
const editor = new Editor()
const mobile = new Mobile({
    ...options,
})
```

-   参数

| 名称          | 类型          | 默认值          | 描述           |
| ------------- | ------------- | --------------- | -------------- |
| `editor`      | `Editor`      | 必选            | 编辑器实例     |
| `container`   | `HTMLElement` | `document.body` | 文档容器       |
| `editorWrap`  | `HTMLElement` | 必选            | 编辑器容器     |
| `commentable` | `boolean`     | `false`         | 是否可评论     |
| `comment`     | `Comment`     | 可选            | 评论插件实例   |
| `upload`      | `boolean`     | `false`         | 是否支持上传   |
| `discord`     | `Discord`     | 可选            | 讨论插件实例   |
| `toolbar`     | `boolean`     | `false`         | 是否启用工具栏 |
