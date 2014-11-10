开发目录规范
==========
###目录结构划分

目录划分规则：

* 一级目录主要按照职能进行划分
* 二级目录主要按照文件类型进行划分

目录结构：
```javascript
.
├── package.json    //声明&配置文件
├── build.sh        //编译脚本
├── src             //源文件目录
    ├── css             //css 样式文件目录
    ├── less            //less 样式文件目录
    ├── js              //js 文件目录
    ├── image           //图片文件目录(可包含png,gif,jpg等)
    ├── swf             //flash文件
    ├── tpl             //smarty后端模板文件
    ├── widget          //组件目录（可能包含一组tpl + js + css + image）
        ├── ui.xxx          //展示类型组件
            ├── main.js         //组件入口文件
            ├── main.css        //组件入口css文件
            ├── README.md       //组件说明文档
├── lib             //前端lib
    ├── jquery.js
    ├── require.js
    ├── bootstrap
        ├── bootstrap.js
        ├── bootstrap.css
├── test            //本地测试文件
├── doc             //模块说明文档
├── output          //编译产出代码
```

### package.json  配置

```javascript
{
    "name": "xxx",                          //模块名称
    "description": "Concatenate files.",    //描述信息
    "version": "1.0.1",                     //模块版本
    "url": "http://qing.baidu.com/xxx",     //对应线上地址
    "author": [{                            //负责人信息
        "name": "xxx",                          //姓名
        "mail": "xxx@xxx.com"                   //邮箱
    }]
}
