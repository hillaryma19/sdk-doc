表格快捷键包含了系统默认快捷键和自定义的快捷键，如下表所示

### 文本格式

| 操作   | MacOs           | 非 MacOs           |
| ------ | --------------- | ------------------ |
| 粗体   | `⌘ + B`         | `Ctrl + B`         |
| 斜体   | `⌘ + I`         | `Ctrl + I`         |
| 下划线 | `⌘ + U`         | `Ctrl + U`         |
| 中划线 | `⌘ + Shift + S` | `Ctrl + Shift + S` |

### 插入

| 操作     | MacOs            | 非 MacOs            |
| -------- | ---------------- | ------------------- |
| 评论     | `⌘ + Shift + M`  | `Ctrl + Shift + M`  |
| 超链接   | `⌘ + K`          | `Ctrl + K`          |
| 当前日期 | `⌘ + ；`         | `Ctrl + ；`         |
| 当前时间 | `⌘ + Shift + ；` | `Ctrl + Shift + ；` |

### 编辑

| 操作         | MacOs              | 非 MacOs           |
| ------------ | ------------------ | ------------------ |
| 撤销         | `⌘ + Z`            | `Ctrl + Z`         |
| 重做         | `⌘ + Y`            | `Ctrl + Y`         |
| 复制         | `⌘ + C`            | `Ctrl + C`         |
| 剪切         | `⌘ + X`            | `Ctrl + X`         |
| 粘贴         | `⌘ + V`            | `Ctrl + V`         |
| 仅粘贴值     | `⌘ + Shift + V`    | `Ctrl + Shift + V` |
| 仅粘贴格式   | `⌘ + Opt + V`      | `Ctrl + Alt + V`   |
| 取消编辑内容 | `Esc`              | `Esc`              |
| 查找         | `⌘ + F`            | `Ctrl + F`         |
| 新增行       | `⌘ + Shift + =`    | `Ctrl + Shift + =` |
| 单元格内换行 | `Ctrl/Opt + Enter` | `Ctrl/Alt + Enter` |
| 激活单元格   | `Enter`            | `Enter`            |
| 合并单元格   | `Opt + Shift + D`  | `Alt + Shift + D`  |

### 操作

| 操作               | MacOs             | 非 MacOs             |
| ------------------ | ----------------- | -------------------- |
| 全选               | `⌘ + A`           | `Ctrl + A`           |
| 选区扩展一个单元格 | `Shift + ↑/↓/←/→` | `Shift + ↑/↓/←/→`    |
| 定位至边缘         | `⌘ + ↑/↓/←/→`     | `Ctrl + ↑/↓/←/→`     |
| 选区扩展至上下边缘 | `⌘ + Shift + ↑/↓` | `Ctrl + Shift + ↑/↓` |
| 选区扩展至左右边缘 | `⌘ + Shift + ←/→` | `Ctrl + Shift + ←/→` |
| 向下填充           | `⌘ + D`           | `Ctrl + D`           |
| 缩放页面           | `Opt + +/-`       | `Alt + +/-`          |

## 构造函数

- 用法

  ```js
  var editor = new shimo.sdk.sheet.Editor();
  var shortcut = new shimo.sdk.sheet.plugins.Shortcut({ editor });
  ```

- 参数

| 名称             | 类型     | 默认值 | 描述       |
| ---------------- | -------- | ------ | ---------- |
| `options.editor` | `Editor` | 必选   | 编辑器实例 |
