#Safari 浏览器

##选择器 Hack
```css
/* Safari 2/3 */
html[xmlns*=""] body:last-child .selector {} 
html[xmlns*=""]:root .selector  {}
/* Safari 2/3.1, Opera 9.25 */
*|html[xmlns*=""] .selector {}
/* Safari 5- and Chrome 24- */
::made-up-pseudo-element, .selector {}
```　　

##媒体查询 Hack
```css
/* Safari 3+, Chrome */
@media screen and (-webkit-min-device-pixel-ratio:0) {}
```　　

##JavaScript Hack
```js
/* Safari */
var isSafari = /a/.__proto__=='//';
```
