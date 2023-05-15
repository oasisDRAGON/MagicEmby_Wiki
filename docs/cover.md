# Cover

Activate the cover feature by setting `coverpage` to **true**. See [coverpage configuration](configuration.md#coverpage).

## Basic usage

Set `coverpage` to **true**, and create a `_coverpage.md`:

```html
<!-- index.html -->

<script>
  window.$docsify = {
    coverpage: true
  }
</script>
<script src="//cdn.jsdelivr.net/npm/docsify/lib/docsify.min.js"></script>
```

```markdown
<!-- _coverpage.md -->

# 欢迎来到魔法✨emby.

> 基于 docsify 构建


[开始阅读](#docsify)


```

## Custom background

The background color is generated randomly by default. You can customize the background color or a background image:

```markdown
<!-- _coverpage.md -->

# docsify <small>3.5</small>

[GitHub](https://github.com/docsifyjs/docsify/)
[Get Started](#quick-start)

<!-- background image -->

![](_media/bg.png)

<!-- background color -->

![color](#f0f0f0)
```

## Coverpage as homepage

Normally, the coverpage and the homepage appear at the same time. Of course, you can also separate the coverpage by [onlyCover option](configuration.md#onlycover).

## Multiple covers

If your docs site is in more than one language, it may be useful to set multiple covers.

For example, your docs structure is like this

```text
.
└── docs
    ├── README.md
    ├── guide.md
    ├── _coverpage.md
    └── zh-cn
        ├── README.md
        └── guide.md
        └── _coverpage.md
```

Now, you can set

```js
window.$docsify = {
  coverpage: ['/', '/zh-cn/']
};
```

Or a special file name

```js
window.$docsify = {
  coverpage: {
    '/': 'cover.md',
    '/zh-cn/': 'cover.md'
  }
};
```
