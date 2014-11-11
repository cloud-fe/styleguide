#组件书写规范

组件标示一组js+css+image来完成一项扩展功能。

* 【强制】组件必须采用异步模块化加载方式，放入widget目录下
* 【强制】组件js书写符合commonjs规范，在编译时编译脚本自动进行`amd`包裹
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
* 【强制】ID生成规范：
```
1）ID为String类型，命名：xxx(模块名)/xxx(模块下组件资源的路径)
2）ID省略.js后缀
```
* 【强制】组件目录下需要有main.js|main.css，表示该组件的入口文件
* 【强制】组件目录下需要有使用markdown语法书写的README.md文件，来进行组件使用方面的相关描述
* 【强制】widget加载方式：
```
1）var xxx = require('xxx(组件ID)');
2）require(['xxx'], function(xxx){});
3）css或者其他类型那个文件按照如下方式引入ID：
    ①  css!common/src/widget/xxx
    ②  tpl!common/src/widget/xxx
```
* 【强制】各模块不可以加载除common和自身以外其他模块的组件
* 【建议】分功能进行组件名区分，例如：
```javascript
ui.xxx      //表示展示类型组件
ext.xxx     //功能扩展类组件
layer.xxx  //弹层类组件
```