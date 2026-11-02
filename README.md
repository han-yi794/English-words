# 高中英语单词朗读

人教版高中英语七册课本、三十六个单元的单词朗读视频索引。选一册、选一个单元，直接跳到 B 站对应的分 P，不用在播放列表里翻。

在线地址：<https://han-yi794.github.io/English-words/>

## 内容

- 必修 第一至三册，选择性必修 第一至四册，共 7 册
- 每册 5 个单元（必修一另有 Welcome Unit），共 36 段视频
- 每条列出单元号、单元主题和视频时长

## 使用

打开页面后点课本封面，或点下方目录里的册名，再点单元即可。页面会记住上次选的是哪一册，下次打开直接停在那册。

也可以直接把 `index.html` 拖进浏览器，从本地打开；页面不依赖网络上的样式、脚本或字体，只有点单元时才会打开 B 站。

## 文件

```text
index.html          页面本身：样式、脚本、36 条链接都在里面
assets/cover-1..7.webp   七册课本封面
assets/favicon.ico      标签页图标（16 / 32 / 48）
assets/favicon.svg      标签页图标（矢量）
assets/apple-touch-icon.png  添加到主屏时的图标（180）
```

## 修改链接

每个单元是一条 `<li class="unit">`：

```html
<li class="unit" style="--i:0"><a href="https://www.bilibili.com/video/BV1Ns4y1R7f2/?p=1" target="_blank" rel="noopener"><span class="u-name">Welcome Unit</span><span class="u-theme">开篇单元</span><span class="u-time">4:25</span><span class="u-go" aria-hidden="true">↗</span></a></li>
```

- `?p=` 后面的数字是 B 站分 P 序号
- `u-name` 是单元号，`u-theme` 是单元主题，`u-time` 是时长
- `style="--i:0"` 控制入场动效的先后，按顺序递增即可

换封面时，用同名的 `cover-N.webp` 覆盖 `assets/` 里的文件，页面不用改。

## 说明

- 单个 HTML 文件，无构建步骤、无外部依赖
- 切册用单选按钮加 CSS 完成，脚本只负责滚动定位、记住选择、随机选一个单元
- 系统开启「减少动态效果」时，入场和滚动动效会自动关闭
- 视频版权归原 UP 主与 B 站所有，本页只做索引和跳转

## 许可

页面代码以 [Apache License 2.0](LICENSE) 发布。课本封面与视频内容的权利归各自权利人。
