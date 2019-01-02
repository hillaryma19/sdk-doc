# 文档快捷键插件

加载此插件，编辑器中可以使用使用快捷键。

## 支持的快捷键列表

* 文字格式

| 操作                | 快捷键                   |
| ------------------- | ------------------------ |
| 粗体              | `⌘ + B`                  |
| 斜体              | `⌘ + I`                  |
| 下划线              | `⌘ + U`                  |
| 中划线              | `⌘ + Shift + S`                  |
| 字号              | `⌘ + Shift + ↑/↓`                  |


* 插入

| 操作                | 快捷键                   |
| ------------------- | ------------------------ |
| 提及某人/ 文件              | `@`                  |
| 划词评论              | `⌘ + Shift + M`                  |
| 位置              | `⌘ + Shift + G`                  |


* markdown 格式

| 操作                | 快捷键                   |
| ------------------- | ------------------------ |
| 标题1              | `# + 空格`                  |
| 标题2              | `## + 空格`                  |
| 标题3              | `### + 空格`                  |
| 有序列表              | `1.+ 空格`                  |
| 无序列表              | `*或- + 空格`                  |
| 任务列表              | `[] + 空格`                  |
| 引用              | `> + 空格`                  |
| 代码块              | ```` + 空格`                  |
| 分隔线              | `--- + 空格`                  |


* 段落格式

| 操作                | 快捷键                   |
| ------------------- | ------------------------ |
| 设置标题              | `⌘ + Shift + K`                  |
| 标题1              | `⌘ + Opt + 1`                  |
| 标题2              | `⌘ + Opt + 2`                  |
| 标题3              | `⌘ + Opt + 3`                  |
| 正文              | `⌘ + Opt + 0`                  |
| 有序列表              | `⌘ + Shift + U`                  |
| 无序列表              | `⌘ + Shift + I`                  |
| 任务列表              | `⌘ + Shift + Y`                  |
| 增加缩进              | `TAB`                  |
| 减少缩进              | `Shift + TAB`                  |


* 编辑

| 操作                | 快捷键                   |
| ------------------- | ------------------------ |
| 撤销              | `⌘ + Z`                  |
| 重做              | `⌘ + Y`                  |
| 查找              | `⌘ + F`                  |
| 查找并替换              | `⌘ + H`                  |


* 操作

| 操作                | 快捷键                   |
| ------------------- | ------------------------ |
| 将当前内容保存为版本              | `⌘ + Opt + S`                  |
| 打开 / 关闭 历史              | `⌘ + Shift + L`                  |
| 打开 / 关闭 目录              | `⌘ + Shift + O`                  |
| 打开 / 关闭 讨论              | `⌘ + Shift + D`                  |
| 进入演示模式              | `⌘ + Shift + P`                  |


## 构造函数

* 用法

```js
const Editor = shimo.sdk.document.Editor
const Shortcut = shimo.sdk.document.plugins.Shortcut
const editor = new Editor()
const shortcut = new Shortcut({
  editor,
  plugins: {
    demoScreen: null,
    revision: null,
    history: null,
    tableOfContent: null
  }
})

editor.render(...)
shortcut.render()
```

* 参数

|名称|类型|默认值|描述|
| -- | -- | -- | -- |
| `editor` | `Editor` | 必选 | 编辑器实例 |
| `plugins.demoScreen` | `DemoScreen` | 可选 | 演示模式插件实例 |
| `plugins.revision` | `Revision` | 可选 | 版本插件实例 |
| `plugins.history` | `History` | 可选 | 历史插件实例 |
| `plugins.tableOfContent` | `TableOfContent` | 可选 | 目录插件实例 |

## 方法列表

## render

渲染初始化。

* 返回 `undefined`
* 用法 `shortcut.render()`

## destroy

使用完销毁。

* 返回 `undefined`
* 用法 `shortcut.destroy()`
