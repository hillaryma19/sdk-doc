# 表格筛选插件

表格筛选插件可以创建筛选，或筛选视图。

## 构造函数

* 用法

  ```js
  var editor = new shimo.sdk.sheet.Editor()
  editor.render({
    content: [表格内容],
    container: [表格渲染容器]
  })

  new window.shimo.sdk.sheet.plugins.FilterViewport({
    editor: editor,
  })

  ```
