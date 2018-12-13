# 文档快捷键插件

加载此插件，编辑器中可以使用使用快捷键。

## 构造函数

* 用法

```js
const Editor = shimo.sdk.document.Editor
const Keyboard = shimo.sdk.document.plugins.Keyboard
const editor = new Editor()
const keyboard = new Keyboard({
  editor,
  plugins: {
    demoScreen: null,
    revision: null,
    history: null,
    tableOfContent: null
  }
})

editor.render(...)
keyboard.render()
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
* 用法 `keyboard.render()`

## destroy

使用完销毁。

* 返回 `undefined`
* 用法 `keyboard.destroy()`
