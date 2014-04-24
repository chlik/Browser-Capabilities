#Chrome 浏览器

##选择器 Hack
```css
/* Chrome 24- and Safari 5- */
::made-up-pseudo-element, .selector {}
```

##媒体查询 Hack
```css
/* Chrome, Safari 3+ */
@media screen and (-webkit-min-device-pixel-ratio:0) {}
```　　

##JavaScript Hack
```js
/* Chrome */
var isChrome = Boolean(window.chrome);
```
