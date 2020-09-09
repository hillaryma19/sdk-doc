# 编辑器

表格编辑器类，提供了获取内容、设置内容、操作表格的方法。

## 构造函数

- 用法

  ```js
  new shimo.sdk.sheet.Editor();
  new shimo.sdk.sheet.Editor(options);
  ```

- 参数

| 名称                                | 类型      | 默认值 | 描述                              |
| ----------------------------------- | --------- | ------ | --------------------------------- |
| `options.editable`                  | `Boolean` | `true` | 设置表格是否只读                  |
| `options.commentable`               | `Boolean` | `true` | 是否允许单元格评论                |
| `options.disableRenderOptimization` | `Boolean` | `true` | 是否禁用表格渲染优化              |
| `options.localeConfig`              | `Object`  | 可选   | 国际化相关配置，如果未传，默认使用中文（zh-CN）  |
| `options.localeConfig.fetchLocaleSync` | `String`  | 可选   | 获取翻译资源的方式  |
| `options.localeConfig.locale`       | `String`  | 可选   |  设置当前要使用的语言，eg: 'en-US' | 
| `options.uploadConfig`              | `Object`  | 可选   | 上传图片配置                      |
| `options.uploadConfig.origin`       | `String`  | 必选   | 上传服务的地址                    |
| `options.uploadConfig.server`       | `String`  | 必选   | 存储服务类型, eg, 'oss', 'aws' |
| `options.uploadConfig.token`        | `String`  | 必选   | 上传服务鉴权秘钥                  |
| `options.downloadConfig`            | `Object`  | 可选   | 下载图片配置                      |
| `options.spellCheck`                | `Boolean` | 可选   | 是否开启拼写检查，默认不开启      |
| `options.fontConfig`                | `Object`  | 可选   | 字体配置                |
| `options.fontConfig.baseUrl`        | `String`  | 可选   | 下载字体的地址                    |
| `options.fontConfig.fontNames`      | `Object`  | 可选   | 字体文件名（地址+文件名）即为完整路径    |
| `options.user`                      | `Object`  | 必选   | 当前用户    |

## 属性列表

| 名称         | 类型      | 描述                    |
| ------------ | --------- | ----------------------- |
| `isRendered` | `Boolean` | 表格是否渲染成功        |
| `spread`     | Spread    | [工作簿实例](spread.md) |

## 方法列表

### render

渲染表格。

- 返回 `undefined`
- 用法 `render(options)`
- 参数

| 名称                | 类型          | 默认值 | 描述         |
| ------------------- | ------------- | ------ | ------------ |
| `options.content`   | `string`      | 无     | 表格内容     |
| `options.container` | `HTMLElement` | 无     | 表格渲染容器 |
| `options.activeSheetId` | `string` | 可选     | 需激活的工作表 ID |
| `options.userId` | `number` | 可选     | 当前用户 ID，用于历史插件展示 |

### getContent

获取表格内容。

- 返回 `Promise<string>`
- 用法

```js
editor.getContent().then(function(content) {
  console.log(content);
});
```

### setContent

设置表格内容。

- 返回 `undefined`
- 用法 `setContent(content, activeSheetId)`
- 参数

| 名称            | 类型     | 默认值 | 描述                      |
| --------------- | -------- | ------ | ------------------------- |
| `content`       | `String` | 无     | 表格内容                  |
| `activeSheetId` | `String` | 无     | 设置表格先渲染的工作表 ID |

### destroy

销毁表格编辑器实例。

- 返回 `undefined`
- 用法 `destroy()`
- 参数

### undo

撤销上一步操作。

- 返回 `Promise<undefined>`
- 用法

```js
editor.undo().then(function() {
  console.log("undo successed!");
});
```

- 参数

### redo

重新应用上一步操作。

- 返回 `Promise<undefined>`
- 用法

```js
editor.redo().then(function() {
  console.log("redo successed!");
});
```

- 参数


### getLocale

获取当前语言。

- 返回 `string`
- 用法

```js
const currentLocale = editor.getLocale()  // eg: en-US、zh-CN
```

- 参数
