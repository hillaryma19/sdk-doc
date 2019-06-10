# 表格事件

表格内部事件，可以监听对应事件，添加相应逻辑


* 用法

### 表格内容改变事件

  ```js
  var editor = new shimo.sdk.sheet.Editor()
  var events = shimo.sdk.sheet.Editor.events
  editor.on(events.CHANGE, function() {
    // your code
  })
  ```

### 表格出现异常事件
  ```js
  var editor = new shimo.sdk.sheet.Editor()
  var events = shimo.sdk.sheet.Editor.events
  editor.on(events.ERROR, function(msg) {
    // 表格出错后请中断编辑，刷新后继续使用
  })
  ```
* 表格出现异常事件参数

| 名称               | 类型        | 描述             |
| ------------------ | --------- | ---------------- |
| `msg` | `String`  | 错误原因 |


### 切换工作表事件

  ```js
  var editor = new shimo.sdk.sheet.Editor()
  var events = shimo.sdk.sheet.Editor.events
  editor.on(events.SHEET_SWITCHED, function(args) {
    // your code
  })
  ```

* 切换工作表事件回调函数参数

| 名称               | 类型        | 描述             |
| ------------------ | --------- | ---------------- |
| `args.newSheet` | `Sheet`  | 新激活的工作表 |
| `args.oldSheet` | `Sheet`  | 旧工作表 |


### 工作表列表更新事件

  ```js
  var editor = new shimo.sdk.sheet.Editor()
  var events = shimo.sdk.sheet.Editor.events
  editor.on(events.SHEET_TAB_LIST_UPDATED, function() {
    // your code
  })
  ```