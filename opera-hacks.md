#Opera 浏览器

##选择器 Hack
```css
/* Opera 9.25, Safari 2/3.1 */
*|html[xmlns*=""] .selector {}
/* Opera 9.27 and below, Safari 2 */
html:first-child .selector {}
/* Opera 9.5+ */
noindex:-o-prefocus, .selector {}
```　　

##媒体查询 Hack
```css
/* Opera 7 */
@media all and (min-width: 0px){}
/* Opera 12- */
@media all and (-webkit-min-device-pixel-ratio:10000), not all and (-webkit-min-device-pixel-ratio:0) {}
/* Opera, Firefox 3.5+, IE 9/10 */
@media screen and (min-resolution: +72dpi) {}
/* Opera, IE 8/9/10 */
@media screen {}
```　　

##JavaScript Hack
```js
/* Opera 9.64- */
var isOpera = /^function \(/.test([].sort);
/* Opera 12- */
var isOpera = Boolean(window.opera);
```
