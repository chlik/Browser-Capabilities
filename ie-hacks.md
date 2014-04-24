
##IE 选择器 Hack
```css
/* IE 6 and below */
* html .selector  {} 
.suckyie6.selector {} /* .suckyie6 can be any unused class */
/* IE 7 and below */
.selector, {}
/* IE 7 */
*:first-child+html .selector {} 
.selector, x:-IE7 {} 
*+html .selector {}
/* Everything but IE 6 */
html > body .selector {}
/* Everything but IE 6/7 */
html > /**/ body .selector {}
head ~ /* */ body .selector {}
/* Everything but IE 6/7/8 */
:root *> .selector {} 
body:last-child .selector {} 
body:nth-of-type(1) .selector {} 
body:first-of-type .selector {}
```

##IE 属性/值 Hack
```css
/* IE 6 */
.selector { _color: blue; } 
.selector { -color: blue; }
/* IE 6/7 - acts as an !important */
.selector { color: blue !ie; } 
/* string after ! can be anything */
/* IE 6/7 - any combination of these characters: 
 ! $ & * ( ) = % + @ , . / ` [ ] # ~ ? : < > | */
.selector { !color: blue; } 
.selector { $color: blue; } 
.selector { &color: blue; } 
.selector { *color: blue; } 
/* ... */
/* IE 8/9 */
.selector { color: blue\0/; } 
/* must go at the END of all rules */
/* IE 9/10 */
.selector:nth-of-type(1n) { color: blue\9; }
/* IE 6/7/8/9/10 */
.selector { color: blue\9; } 
.selector { color/*\**/: blue\9; }
/* Everything but IE 6 */
.selector { color/**/: blue; }
```

##IE Media Query Hack
```css

/* IE 6/7 */
@media screen\9 {}
/* IE 8 */
@media \0screen {}
/* IE 9/10, Firefox 3.5+, Opera */
@media screen and (min-resolution: +72dpi) {}
/* IE 10+ */
@media screen and (-ms-high-contrast: active), (-ms-high-contrast: none) {}
/* IE 6/7/8 */
@media \0screen\,screen\9 {}
/* IE 8/9/10 & Opera */
@media screen\0 {}
/* IE 9/10 */
@media screen and (min-width:0\0) {}
/* Everything but IE 6/7/8 */
@media screen and (min-width: 400px) {}
```

##IE JavaScript Hack
```js
/* IE 6 */
(checkIE = document.createElement("b")).innerHTML = "<!--[if IE 6]><i></i><![endif]-->"; 
var isIE = checkIE.getElementsByTagName("i").length == 1;
/* IE 7 */
(checkIE = document.createElement("b")).innerHTML = "<!--[if IE 7]><i></i><![endif]-->"; 
var isIE = checkIE.getElementsByTagName("i").length == 1;
navigator.appVersion.indexOf("MSIE 7.")!=-1
/* IE <= 8 */
var isIE = '\v'=='v';
/* IE 8 */
(checkIE = document.createElement("b")).innerHTML = "<!--[if IE 8]><i></i><![endif]-->"; 
var isIE = checkIE.getElementsByTagName("i").length == 1;
/* IE 9 */
(checkIE = document.createElement("b")).innerHTML = "<!--[if IE 9]><i></i><![endif]-->"; 
var isIE = checkIE.getElementsByTagName("i").length == 1;
/* IE 10 */
var isIE = eval("/*@cc_on!@*/false") && document.documentMode === 10;
/* IE 10 */
var isIE = document.body.style.msTouchAction != undefined;
```
