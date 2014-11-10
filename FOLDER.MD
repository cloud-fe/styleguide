开发目录规范
==========

```javascript
.
├── [package.json](#package.json)    //声明&配置文件
├── build.sh        //编译文件
├── README.md       //模块说明目录
├── css             //样式文件目录(可包含css,less等)
    ├── lib             //引入外部css库
├── js              //js 文件目录
    ├── lib            //引入外部js库
├── image           //图片文件目录(可包含png,gif,jpg等)
    ├── lib             //引入外部js库
├── swf             //flash文件
├── tpl             //smarty模板文件
├── widget          //组件目录（可能包含一组tpl + js + css + image）
    ├── ui.xxx          //展示类型组件
        ├── main.js         //组件入口文件
        ├── main.css        //组件入口css文件
        ├── README.md       //组件说明文档
├── test  //本地测试文件
├── doc  //模块说明文档

```

### package.json
