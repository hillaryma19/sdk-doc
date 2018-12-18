# 表格图表插件

## 构造函数

* 用法

  ```js
  var editor = new shimo.sdk.sheet.Editor()
  const contextmenu = new window.shimo.sdk.sheet.plugins.Chart({
    editor: editor
  })
  ```

* 参数

|名称|类型|默认值|描述|
| -- | -- | -- | -- |
| `options.editor` | `Editor` | 必选 | 编辑器实例 |