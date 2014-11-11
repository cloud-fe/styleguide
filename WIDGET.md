#组件书写规范

组件标示一组js+css+image来完成一项扩展功能。

* 【强制】组件必须采用异步模块化加载方式，放入widget目录下
* 【强制】组件书写符合commonjs规范，在编译时编译脚本自动进行`amd`包裹
```javascript
var xxx = require('common/src/widget/xxx');
var _init = function(){
    //...
};
module.exports = {
    init: _init
};

//-->
define('xxx', function(require, exports, module){
    var xxx = require('common/src/widget/xxx');
    var _init = function(){
        //...
    };
    module.exports = {
        init: _init
    };
});
```
* 【强制】脚本生成ID规范：
```
1）String类型：xxx(模块名)/xxx(模块下文件路径)
2）ID省略.js后缀
```
* 【强制】widget加载方式：
```
1）var xxx = require('xxx');
2）require(['xxx'], function(xxx){});
3）css或者其他类型那个文件按照如下方式引入ID：
    ①  css!common/src/widget/xxx
    ②  tpl!common/src/tidget/xxx
```
