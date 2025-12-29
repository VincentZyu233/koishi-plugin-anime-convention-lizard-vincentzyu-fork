# koishi-plugin-anime-convention-lizard-vincentzyu-fork
> **上游仓库**：[https://github.com/lizard0126/anime-convention-lizard](https://github.com/lizard0126/anime-convention-lizard)

## 💬 反馈与交流
- **QQ 交流群**：259248174

## 🎉 开箱即用的漫展查询插件
[![npm](https://img.shields.io/npm/v/koishi-plugin-anime-convention-lizard-vincentzyu-fork?style=flat-square)](https://www.npmjs.com/package/koishi-plugin-anime-convention-lizard-vincentzyu-fork)
[![npm-download](https://img.shields.io/npm/dm/koishi-plugin-anime-convention-lizard-vincentzyu-fork?style=flat-square)](https://www.npmjs.com/package/koishi-plugin-anime-convention-lizard-vincentzyu-fork)

**anime-convention-lizard-vincentzyu-fork** 是一款针对漫展查询与订阅的 Koishi 插件。对接 **无差别同人站 (www.allcpp.cn)**，通过简单的指令快速查询城市或主题相关的漫展，并提供订阅与管理功能。

---

## ✨ 特性

- 🔍 **多维查询**：支持按城市名或漫展主题关键词进行搜索。
- 📅 **订阅系统**：订阅感兴趣的关键词，一键获取所有关注城市的漫展动态。
- 🖼️ **精美渲染**：支持通过 Puppeteer 将查询结果渲染为精美图片（可选）。
- 🔤 **自定义字体**：支持加载本地字体文件，让图片渲染更符合你的审美。
- 🚀 **自托管后端**：支持配置自定义后端 API，稳定可靠。

## 🔍 预览
![https://gitee.com/vincent-zyu/koishi-plugin-anime-convention-lizard-vincentzyu-fork/releases/download/preview2/list-preview.png](https://gitee.com/vincent-zyu/koishi-plugin-anime-convention-lizard-vincentzyu-fork/releases/download/preview2/list-preview.png)
![https://gitee.com/vincent-zyu/koishi-plugin-anime-convention-lizard-vincentzyu-fork/releases/download/preview2/detail-preview.png](https://gitee.com/vincent-zyu/koishi-plugin-anime-convention-lizard-vincentzyu-fork/releases/download/preview2/detail-preview.png)

---

## 📦 安装

在 Koishi webui的`插件市场`中搜索插件名`anime-convention-lizard-vincentzyu-fork` 并安装。

或者 Koishi webui的`依赖管理`中搜索npm包名`koishi-plugin-anime-convention-lizard-vincentzyu-fork` 并安装。

或者使用 npm/yarn：

```bash
npm install koishi-plugin-anime-convention-lizard-vincentzyu-fork
yarn add koishi-plugin-anime-convention-lizard-vincentzyu-fork
```

### 🛠️ 前置依赖
- **必须依赖**：`database` (用于存储订阅信息)
- **可选依赖**：`puppeteer` (用于图片渲染功能)
  - 推荐安装：`koishi-plugin-puppeteer` 或 `@shangxueink/koishi-plugin-puppeteer-without-canvas`

---

## ⚙️ 配置说明

### 🔗 后端 API
本插件默认使用作者提供的公共 API。

```typescript
// 默认配置
apiUrl: Schema.string()
    .default('http://xwl.vincentzyu233.cn:51225/search')
    .description('后端api地址'),
```

如果你希望自托管后端，可以前往 [https://github.com/VincentZyu233/allcpp-search-go](https://github.com/VincentZyu233/allcpp-search-go) 下载二进制文件直接运行。或者你自己用源码go build一份也行( 这个后端他就是直接请求www.allcpp.cn的接口的


### 🔤 字体设置
你可以手动下载字体文件，并在插件配置项中填写字体的**绝对路径**。

**推荐字体：**
- [落霞孤鹜文楷 LXGW WenKai Mono → *(https://gitee.com/vincent-zyu/koishi-plugin-onebot-info-image/releases/download/font/LXGWWenKaiMono-Regular.ttf)*](https://gitee.com/vincent-zyu/koishi-plugin-onebot-info-image/releases/download/font/LXGWWenKaiMono-Regular.ttf)
- [思源宋体 Source Han Serif SC → *(https://gitee.com/vincent-zyu/koishi-plugin-onebot-info-image/releases/download/font/SourceHanSerifSC-Medium.otf)*](https://gitee.com/vincent-zyu/koishi-plugin-onebot-info-image/releases/download/font/SourceHanSerifSC-Medium.otf)

> 💡 **提示**：如未填写或路径无效，将自动回退为系统默认字体。

---

## 📖 使用方法

### 🔍 漫展查询
| 指令 | 说明 | 示例 |
| :--- | :--- | :--- |
| `漫展 查询 <关键词>` | 查询指定城市或主题的漫展 | `漫展 查询 南京` |
| `漫展 一键查询` | 查询所有已订阅关键词的漫展 | `漫展 一键查询` |
| `漫展 图片查询 <关键词>` | 以图片形式展示查询结果 | `漫展 图片查询 东方` |
| `漫展 一键图片查询` | 以图片形式展示所有订阅结果 | `漫展 一键图片查询` |

### 📌 订阅管理
| 指令 | 说明 | 示例 |
| :--- | :--- | :--- |
| `漫展 订阅 <关键词>` | 订阅指定关键词 | `漫展 订阅 上海` |
| `漫展 取消订阅 <关键词>` | 取消订阅指定关键词 | `漫展 取消订阅 上海` |
| `漫展 取消订阅` | 清空所有订阅 | `漫展 取消订阅` |
| `漫展 订阅列表` | 查看当前订阅的关键词 | `漫展 订阅列表` |

---

## ☕ 原作者留下的
如果这个插件对你有帮助，可以[请我喝杯可乐🥤 *(https://ifdian.net/a/lizard0126)* ](https://ifdian.net/a/lizard0126) 

