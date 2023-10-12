# Hexo-Theme-Foundation
本项目从 [hexo-theme-yuzu](https://github.com/Cerallin/hexo-theme-yuzu) fork 出来，尝试摸索主题制作，但主要是给幻报用。

**当前分支为 v3.x 版本**，使用pug代替ejs作为模板引擎。


**注意** 需要安装`hexo-renderer-pug`。将鼠标悬停在网页页脚`Theme Foundation`上可以查看当前主题版本。

## 安装使用

```shell
# 在hexo网站源码目录下执行
$ npm i hexo-renderer-pug
$ mkdir -p themes && cd themes
$ git clone https://github.com/GrassBlock1/hexo-theme-foundation foundation
```

将 `config.yml` 中 `theme` 字段改为`foundation`即可，如果你希望独立管理配置，可以将本项目的 `_config.yml` 复制到站点根目录并重命名为 `_config.foundation.yml` 。

**如果你将网站部署到了一个子目录（如 https://example.org/blog ），为了使图标正常显示，请按实际情况修改主题配置中的`site_root`参数**

## 示例网站

- [基石](https://sci-fic.xyz)


## 特色
- 黑白色调，风格质朴简约。
- 针对文章创作优化，学术博客也是可以的 (?)。
- 支持深色模式，自适应电脑/手机深浅色模式。

## 功能
- 支持分页（hexo-generator-*）
- 适配搜索（hexo-generator-search）
- 支持显示 CC（Creative Commons）版权声明
- 文章文字两端对齐
- 适配学术写作（pandoc）

## 禁止用户复制粘贴网页内容

**注** 本选项仅为君子协定，通过插件可以轻易破解。
将主题配置文件中的`selectable`值改为`false`。

## 深色模式

将主题配置文件中的`dark_mode`值改为`true`。

## 学术写作指南

请先安装`hexo-renderer-pandoc`。

### 三线表格

```md
| key          | value                    |  type   |
| :----------- | :----------------------- | :-----: |
| num          | 65535                    | integer |
| post         | {id: 4, content: "text"} | object  |
| article_list | [{id: 1}, {id: 2}]       |  array  |
: 表格名 {#ref:tbl-name}
```

### 图

```md
![figure description](/path/to/figure.jpg){#ref:fig-name}
```

### 推荐插件

- hexo-filter-mathjax: 渲染生成mathjax公式；
- [hexo-filter-text-autospace](https://github.com/cerallin/hexo-filter-text-autospace): 为中文段落中的英文自动添加间距。
- hexo-clean-css：缩小生成的CSS文件的体积。由于Stylus自身的限制，本主题的CSS文件大小有很大的缩减空间。

## [辅助工具类](./docs/helpers.md)

本主题提供了一些类似tailwind css的辅助工具类。

例如，通过`text-{left|right|justify}`控制文字对齐，使用 `m{t|r|b|l}-{size}` 功能类控制元素一侧的外边距等等。

详细介绍请移步[这里](./docs/helpers.md)。

## TODOs

- [ ] 整理主题变量
- [ ] 重构模板布局，优化模板缓存
- [ ] 开发“关于”页的模板
- [ ] 更多动画
- [ ] 更多的helpers类

## License

This project is under MIT License.

    Copyright (c) 2021-2023 Cerallin   <cerallin@cerallin.top>

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.

### Bootstrap icons

Part of [Bootstrap opensource SVG icon library](https://github.com/twbs/icons) is used in this project, which is under MIT license.

### Clipboard.js

[Clipboard.js](https://github.com/zenorocha/clipboard.js) is used in this project, which is under MIT license.

### Smooth-corners.js

[Smooth-corners.js](https://github.com/wopian/smooth-corners) is used in this project, which is under MIT license.
