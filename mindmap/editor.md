# 石墨文档思维导图 SDK

版本号 0.4.0

## 注意事项

1. 需要额外引入 `vue` 依赖。
2. 默认输出的 SMMindmap 就是四件套通常意义上的 `Editor`
3. content 为 null/undefined 的时候会渲染一个空的视图，此时 getContent 返回 `(new Delta([])).stringify()`, 即 `'0:'`
4. 初始化的时候可以不传 `options.file` ，此时会渲染空视图

## 构造函数

- 用法

  ```js
  new SMMindmap({
    file:
      '1b:19!11@Z00000001q#h:g!b@D8:7!4!中心主题 0["C*0"] 0 1["$aautoLayout1","$crootTopicIds:00000001"]',
  })
  ```

- 参数

| 名称           | 类型                                         | 默认值 | 描述                                                                |
| -------------- | -------------------------------------------- | ------ | ------------------------------------------------------------------- |
| `options.file` | `Delta or modoc string or null or undefined` | 无     | 设置思维导图初始化渲染数据，为 undefined 或者 null 的时候渲染空视图 |

## 方法列表

### render

渲染思维导图内容，返回一个 Promise，渲染完成后 resolve

- 返回 `Promise<undefined>`
- 用法 `render(container, renderOptions)`
- 参数

| 名称                        | 类型                  | 默认值 | 描述                                          |
| --------------------------- | --------------------- | ------ | --------------------------------------------- |
| `container`                 | `HTMLElement`         | 无     | 思维导图渲染容器                              |
| `renderOptions`             | `Object or undefined` | 无     | 渲染配置项                                    |
| `renderOptions.open`        | `Boolean`             | false  | 公开或者协作                                  |
| `renderOptions.readable`    | `Boolean`             | true   | 可读                                          |
| `renderOptions.commentable` | `Boolean`             | false  | 可评论                                        |
| `renderOptions.editable`    | `Boolean`             | false  | 可编辑                                        |
| `renderOptions.selectable`  | `Boolean`             | true   | 可选择                                        |
| `renderOptions.touchable`   | `Boolean`             | false  | 是否触屏，影响 tooltips 等和 hover 相关的功能 |

### renderSheet

只渲染画布，参数返回同 `render`

### destroy

销毁思维导图编辑器实例。

- 返回 `void`
- 用法 `destroy()`
- 参数 无

### onceReady

返回一个 Promise，渲染完成后 resolve

- 返回 `Promise<undefined>`
- 用法 `onceReady().then()`
- 参数 无

### centerTopic

居中给定主题节点

- 返回 `void`
- 用法 `centerTopic('00000001')`
- 参数

| 名称      | 类型     | 默认值 | 描述                |
| --------- | -------- | ------ | ------------------- |
| `topicId` | `string` | 无     | 被居中的主题节点 id |

### setContent

设置文件内容，返回一个 Promise，渲染完成后 resolve

- 返回 `Promise<undefined>`
- 用法 `setContent('1b:19!11@Z00000001q#h:g!b@D8:7!4!中心主题 0["C*0"] 0 1["$aautoLayout1","$crootTopicIds:00000001"]')`
- 参数

| 名称      | 类型                                         | 默认值 | 描述             |
| --------- | -------------------------------------------- | ------ | ---------------- |
| `content` | `Delta or modoc string or null or undefined` | 无     | 思维导图文件内容 |

### getContent

返回文件内容

- 返回 `Promise<modoc string>`
- 用法 `getContent()`
- 参数 无

### applyChange

应用更新，返回一个 Promise，渲染完成后 resolve

- 返回 `Promise<undefined>`
- 用法 `applyChange(delta)`
- 参数

| 名称    | 类型                    | 默认值 | 描述             |
| ------- | ----------------------- | ------ | ---------------- |
| `delta` | `Delta or modoc string` | 无     | 思维导图更新内容 |

### updateOptions

四件套统一，切换可编辑模式，返回一个 Promise，渲染完成后 resolve

- 返回 `Promise<undefined>`
- 用法 `updateOptions(options)`
- 参数

| 名称               | 类型      | 默认值 | 描述       |
| ------------------ | --------- | ------ | ---------- |
| `options`          | `Object`  | 无     | 配置项     |
| `options.editable` | `Boolean` | 无     | 是否可编辑 |

## 事件列表

- 用法

  ```js
  const events = editor.events
  editor.on(events.CHANGE, handler)
  ```

### CHANGE

数据变化

- 回调方法签名 `handler(delta)`
- 参数

| 名称    | 类型    | 默认值 | 描述 |
| ------- | ------- | ------ | ---- |
| `delta` | `Delta` | 无     | 数据 |

### READY

渲染结束，每次数据变更都会触发一次 READY 事件

- 回调方法签名 `handler()`
- 参数 无
