---
sidebar: auto
---

# package.json

## dependencies

### interactjs
使用JavaScript实现拖放、缩放和多点触控手势
InteractJS是一个JavaScript模块，它为最新的浏览器（包括IE8以上版本）增加了拖放、缩放和多点触控手势，并带有惯性和快照功能。
这个库的主要目的是替换jQuery UI所提供的功能。 因此，使用InteractJS来编写的web应用在智能手机和平板上会更加易用。 InteractJS是一个轻量级的库，可以与SVG技术协作，处理多点触控输入，而把渲染元素以及设置其样式的任务留给了应用程序。

官网：[https://interactjs.io/](https://interactjs.io/)

### element-resize-detector
vue中监控元素大小变化
#### RemoveListener(element，listener)
从元素中移除侦听器。
#### RemoveAllListener(element)
从元素中移除所有侦听器，但不完全删除检测器。如果以后可能会添加侦听器，并且不希望检测器再次初始化，请使用此函数。
#### uninstall(element)
完全删除检测器和所有侦听器。

## devDependencies

### babel-plugin-transform-flow-comments

Turn flow type annotations into comments.

You should be able to use this plugin instead of babel-plugin-flow-strip-types to preserve the /* @flow */ directive and still use flow.

[http://flowtype.org/blog/2015/02/20/Flow-Comments.html](http://flowtype.org/blog/2015/02/20/Flow-Comments.html)

**Example**

In
```js
function foo(bar?) {}
function foo2(bar?: string) {}
function foo(x: number): string {}
type B = {
  name: string;
};
export type GraphQLFormattedError = number;
import type A, { B, C } from './types';
import typeof D, { E, F } from './types';
```

Out
```js
"use strict";

function foo(bar /*:: ?*/) {}
function foo2(bar /*:: ?: string*/) {}
function foo(x /*: number*/) /*: string*/ {}
/*:: type B = {
  name: string;
};*/
/*:: export type GraphQLFormattedError = number;*/
/*:: import type A, { B, C } from './types';*/
/*:: import typeof D, { E, F } from './types';*/
```

#### babel.config.js
```js
"plugins": [
    "transform-flow-comments"
  ]
```

### node-sass
Node-sass是一个库，它将Node.js绑定到LibSass（流行样式表预处理器Sass的C版本）。它允许用户以令人难以置信的速度将.scss文件本地编译为css，并通过连接中间件自动编译。

Sass是一种预处理器脚本语言，可以解释或编译成层叠样式表（CSS）。

Sass包含两种语法：较旧的语法使用缩进将代码块和换行符分隔为单独的规则；较新的语法SCSS使用像CSS这样的块格式。它使用大括号来表示代码块和分号来分隔块中的行。

缩进语法和SCSS文件传统上分别给出扩展名.sass和.scss

### sass-loader
Loads a SASS/SCSS file and compiles it to CSS.

sass-loader依赖于node-sass,所以要安装node-sass
