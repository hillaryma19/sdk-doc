# 石墨文档思维导图 SDK

## 构造函数

- 用法

  ```js
  new SMMindmap.Editor(options);
  ```

- 参数

| 名称                  | 类型           | 默认值                                                                                                | 描述                       |
| --------------------- | -------------- | ----------------------------------------------------------------------------------------------------- | -------------------------- |
| `options.fileContent` | `modoc string` | `'1b:19!11@Z00000001q#h:g!b@D8:7!4!中心主题 0["C*0"] 0 1["$aautoLayout1","$crootTopicIds:00000001"']` | 设置思维导图初始化渲染数据 |

## 方法列表

### render

渲染思维导图内容。

- 返回 `void`
- 用法 `render(container, options)`
- 参数

| 名称                             | 类型          | 默认值 | 描述               |
| -------------------------------- | ------------- | ------ | ------------------ |
| `container`                      | `HTMLElement` | 无     | 思维导图渲染容器   |
| `options`                        | `Object`      | 无     | 渲染配置项         |
| `options.permission`             | `Object`      | 无     | 权限设置           |
| `options.permission.open`        | `Boolean`     | false  | 公开或者协作       |
| `options.permission.readable`    | `Boolean`     | false  | 可读               |
| `options.permission.commentable` | `Boolean`     | false  | 可评论             |
| `options.permission.editable`    | `Boolean`     | false  | 可编辑             |
| `options.layout`                 | `Object`      | 无     | 布局设置           |
| `options.layout.toolbar`         | `Boolean`     | false  | 是否显示顶部工具栏 |

### destroy

销毁思维导图编辑器实例。

- 返回 `void`
- 用法 `destroy()`
- 参数 无

### setContent

设置文件内容

- 返回 `void`
- 用法 `setContent(content)`
- 参数

| 名称      | 类型           | 默认值 | 描述             |
| --------- | -------------- | ------ | ---------------- |
| `content` | `modoc string` | 无     | 思维导图文件内容 |

### getContent

返回文件内容

- 返回 `Promise<modoc string>`
- 用法 `getContent()`
- 参数 无

### applyChange

应用更新

- 返回 `void`
- 用法 `applyChange(delta)`
- 参数

| 名称    | 类型           | 默认值 | 描述             |
| ------- | -------------- | ------ | ---------------- |
| `delta` | `modoc string` | 无     | 思维导图更新内容 |

### getContentWidthHeight

获取文件渲染后的宽高，会在文件渲染结束后 resolve promise

- 返回 `Promise<{ width: number, height: number }>`
- 用法 `getContentWidthHeight()`
- 参数 无

### clearSelection

在文件渲染结束后取消选中状态

- 返回 `Promise`
- 用法 `clearSelection()`
- 参数 无

## 事件列表

- 用法

  ```js
  const events = editor.events;
  editor.on(events.CHANGE, handler);
  ```

### CHANGE

数据变化

- 回调方法签名 `handler(delta)`
- 参数

| 名称    | 类型    | 默认值 | 描述 |
| ------- | ------- | ------ | ---- |
| `delta` | `Delta` | 无     | 数据 |

### READY

渲染结束。READY 事件可能触发多次，触发之后表示当次渲染结束了可以使用。

- 回调方法签名 `handler()`
- 参数 无
