# CSS 的一些新奇用法（个人向）

### pointer-events

[文档](https://developer.mozilla.org/zh-CN/docs/Web/CSS/pointer-events)

禁用鼠标事件

> 事件穿透，如果在该元素的下面还有元素存在，那么会触发下面元素的鼠标事件。

```css
.css {
    pointer-events: none;
}
```

