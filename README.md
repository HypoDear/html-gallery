# html-gallery

单页 HTML 小项目合集。纯静态、零依赖、开箱即玩。

每个项目都是独立目录下的**单个 HTML 文件**，不依赖任何框架、构建工具或网络资源。
离线可用，直接双击也能开。

## 项目列表

| 项目 | 说明 | 在线访问 |
|------|------|----------|
| [海珠雨后 · 体素小世界](voxel-haizhu/) | 雨停后的广州海珠，可环顾的 WebGL 体素场景 | [打开](https://hypodear.github.io/html-gallery/voxel-haizhu/) |

## 在线地址

https://hypodear.github.io/html-gallery/

## 新增项目

1. 新建目录 `<slug>/`，把 HTML 存成 `<slug>/index.html`
2. 在根目录 `index.html` 的 `PROJECTS` 数组里追加一条：

```javascript
{
  slug: 'my-project',          // 目录名，链接会指向 /my-project/
  name: '项目名',
  en: 'English Name',
  tag: '分类标签',
  desc: '一句话说明，会显示在卡片上。',
  meta: '技术 · 交互提示',
  hue: 200,                     // 卡片配色 0–360（青 200、紫 262、琥珀 38、绿 148、红 8）
  size: 'card',                 // 'hero' 占满一行作主推，默认 'card'
  icon: '<path d="…"/>',        // 24×24 viewBox 的 SVG 路径
}
```

3. 在本文件的项目列表里追加一行

**目前只有一个项目，所以它用了 `hero`。** 以后加到两个以上时，可以把新项目设成 `card`，
`hero` 保留给最想让人先点开的那个；卡片数量为奇数时最后一张会自动占满整行。

## 目录约定

```
index.html          合集页
<slug>/index.html   单文件项目
```

用**目录 + index.html** 而不是 `<slug>.html`，是为了让地址栏是干净的 `/my-project/`；
Pages 会自动把目录请求映射到其中的 `index.html`，不需要额外配置。

## Pages

仓库设置 → Pages → Source 选 `Deploy from a branch`，分支 `main`，目录 `/ (root)`。
根目录的 `.nojekyll` 会让 Pages 跳过 Jekyll 处理，避免下划线开头的文件名被忽略。
