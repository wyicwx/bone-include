# bone-act-include
> bone的include文件处理器

[![travis](https://api.travis-ci.org/wyicwx/bone-act-include.png)](https://travis-ci.org/wyicwx/bone-act-include) [![Coverage Status](https://coveralls.io/repos/wyicwx/bone-act-include/badge.png?branch=master)](https://coveralls.io/r/wyicwx/bone-act-include?branch=master)

### 安装及使用

通过npm安装

```sh
$ npm install bone-act-include 
```

安装后在`bonefile.js`文件内通过`act()`加载

```js
var bone = require('bone');
var include = require('bone-act-include');

bone.dest('dist')
	.src('~/src/main.js')
	.act(include);
```

### 说明

支持在任意文件中include其他文件，处理器执行后会替换include为对应文件，并合并成一个文件

调用方式:

+ html标签式

```html
<script type="text/javascript">
	<include file="./jquery.js">
</script>
```

+ 注释式

```js
/**
 include('./lib/jquery.js')
 */

//include('./lib/jquery.js')
```

### 其他

处理器开发以及使用请参考[处理器](https://github.com/wyicwx/bone/blob/master/docs/plugin.md)