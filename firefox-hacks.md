#Firefox 浏览器

##选择器 Hack
```css
/* Firefox 1.5 */
body:empty .selector {}
/* Firefox 2+ */
.selector, x:-moz-any-link {}
/* Firefox 3+ */
.selector, x:-moz-any-link; x:default {}
/* Firefox 3.5+ */
body:not(:-moz-handler-blocked) .selector {}
```

##媒体查询 Hack
```css
/* Firefox 3.5+, IE 9/10, Opera */
@media screen and (min-resolution: +72dpi) {}
/* Firefox 3.6+ */
@media screen and (-moz-images-in-menus:0) {}
/* Firefox 4+ */
@media screen and (min--moz-device-pixel-ratio:0) {}
```

##JavaScript Hack
```js
/* Firefox */
var isFF = !!navigator.userAgent.match(/firefox/i);
/* Firefox 2 - 13 */
var isFF = Boolean(window.globalStorage);
/* Firefox 2/3 */
var isFF = /a/[-1]=='a';
/* Firefox 3 */
var isFF = (function x(){})[-5]=='x';
```
