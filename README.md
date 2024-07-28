# Hugo Theme Farallon Simple

Hugo 主题 Farallon的简单修改版，[博客](https://taosky.org/)自用。

目前修改自0.4.4版本，详情见： [bigfa/hugo-theme-farallon](https://github.com/bigfa/hugo-theme-farallon)


### 使用说明
#### config.toml
参照`config.sample.toml`设置，用不到的可以注释掉。

#### 相册
创建`assets/photos`目录，将照片重命名为`日期 标签-标题.后缀`格式，如`2014-05-10 动物-宿舍的猫.jpg`。

默认标签有`日常、风景、物品、动物、饮食`，可以在主题`layouts/_default/photos.html`修改。

最后新建`content/page/photos.md`：

````markdown
---
title: 相册
layout: "photos"
slug: "photos"
url: "/photos"
comments: false
---
````

#### 看过

需自行搭建后端，见：https://github.com/Taosky/douban

修改`config.toml`的`dbAPIBase`，

新建`content/page/watch.md`：

````markdown
---
layout: "watch"
url: "/watch"
---
````

#### 关于

`content/page/about.md`：

````markdown
---
title: "关于"
layout: "about"
url: "/about"
comments: true
---
````

#### 友链

`content/page/friends.md`：

````markdown
---
title: "友链"
layout: "links"
url: "/friends"
links:
    [
        {
            "title": "四十五",
            "link": "https://baidushabi.com/",
            "description": "随缘写写",
        },
        {
            "title": "泷涯零点",
            "link": "https://blog.sylingd.com/",
            "description": "不忘初心，方得始终",
        },
    ]
---
````

#### memo

`content/memo/1.md`：

````markdown

---
title: "可省略标题"
date: 2024-06-25T14:06:25+08:00
---
此处字数限制100

````



### 版本更新

#### 0.4.4.2

- 看过页面样式修改、增加评价文字
- 新增相册页面
- 样式修改


#### 0.4.4.1

- 样式修改（代码高亮、暗黑主题、图片显示、字体等）
- 添加代码拷贝按钮
- memo样式修改，字数限制100，仅展示无详情
- 替换搜索方式（检索JSON）
- 替换评论为Giscus
- 关于页面支持评论
- 移除手动切换主题控件（和Giscus样式匹配）
- 移除i18n支持


### 参考
https://github.com/bigfa/hugo-theme-farallon
https://ttys3.dev/blog/hugo-fast-search