# 表格打印插件

表格打印插件可借助浏览器实现对表格内容的预览打印，有分页，打印方向，缩放比例等选项可以设置。

## 构造函数

* 用法

  ```js
  var editor = new shimo.sdk.sheet.Editor()
  editor.render({
    content: [表格内容],
    container: [表格渲染容器]
  })

  var print = new window.shimo.sdk.sheet.plugins.Print({
    editor: editor,
  })
  print.printPopup.showPrintDialog()
 
  ```
