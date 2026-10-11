# yuzhaohai/resources · 图床仓库

个人图片资源仓库（图床），存放站点与项目引用的图片，通过 GitHub Pages / jsDelivr CDN 原样输出。

## 目录

| 目录 | 内容 | 数量 |
| --- | --- | --- |
| `jiliang/` | 照片集 | 40 张 |
| `poem/` | 诗词图集 | 601 张 |

## 引用方式

图片与 HTML 不同，jsDelivr / raw / Pages 均可正常返回图片内容（`.html` 才会被 jsDelivr 按纯文本返回）。

**1. jsDelivr CDN（推荐，带 CDN 缓存）**

```
https://cdn.jsdelivr.net/gh/yuzhaohai/resources@main/poem/xxx.jpg
```

**2. GitHub Pages（需开启）**：仓库 Settings → Pages → Deploy from a branch → `main` / `(root)`

```
https://yuzhaohai.github.io/resources/poem/xxx.jpg
```

**3. raw 直链**

```
https://raw.githubusercontent.com/yuzhaohai/resources/main/poem/xxx.jpg
```

### Markdown 引用示例

```markdown
![图片](https://cdn.jsdelivr.net/gh/yuzhaohai/resources@main/jiliang/xxx.jpg)
```

## 使用流程

1. 把图片放入对应目录（`jiliang/` 或 `poem/`），文件名避免空格和中文（推荐 `字母-数字.jpg` 或 `日期-名称.jpg`）
2. `git add -A && git commit -m "..." && git push`
3. 引用地址：`https://cdn.jsdelivr.net/gh/yuzhaohai/resources@main/<目录>/<文件名>`

## 说明

- 根目录的 `.nojekyll` 关闭 GitHub Pages 的 Jekyll 处理，保证图片按原样输出。
- 仓库需为 **Public** 才能被 Pages / jsDelivr 公开访问。
- 单个文件超过 20MB 时 jsDelivr 会拒绝，超大文件建议压缩后再上传。
