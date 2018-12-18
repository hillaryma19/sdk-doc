# 表格公式侧边栏插件

表格公式列表插件。实例化后将在工具栏【公式】菜单中添加【全部】选项，点击后显示侧边栏，展示石墨表格所支持的全部公式；点击列表内任一公式，可将其插入到当前选中单元格。通过 API 调用也可以显示/隐藏公式列表侧边栏。

## 构造函数

* 用法

  ```js
  var editor = new shimo.sdk.sheet.Editor()
  const contextmenu = new window.shimo.sdk.sheet.plugins.FormulaSidebar({
    editor: editor,
    container: $('#sidebar-container'),
  })
  ```

* 参数

|名称|类型|默认值|描述|
| -- | -- | -- | -- |
| `options.editor` | `Editor` | 必选 | 编辑器实例 |
| `options.container` | `HTMLElement` | 必选 | 侧边栏宿主容器 |

## 方法列表

### show

显示侧边栏。

* 返回 `void`
* 用法 `show()`

### hide

隐藏侧边栏。

* 返回 `void`
* 用法 `hide()`

### render

挂载公式列表侧边栏到指定容器

* 返回 `void`*
* 用法 `render(container: $('#sidebar-container'))`
* 参数

| 名称               | 类型      | 默认值  | 描述             |
| ------------------ | --------- | ------- | ---------------- |
| `container` | `HTMLElement` | 必选 | 公式列表侧边栏容器 |