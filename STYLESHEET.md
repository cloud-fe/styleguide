#样式文件开发规范

####文件命名规范
####选择器命名规范

* 【建议】css文件最外层选择器建议使用class，最外层class命名规范如下
    * common模块下的通用css：g-xxx
    * 模块下css：m(module)-xxx(模块名)-xxx
    * 组件下css：w(widget)-xxx(组件名)-xxx

####代码书写

* 【强制】杜绝!important
* 【建议】单个文件内选择器层级不超过4级
* 【强制】禁止在css中单独设置@charset
* 【强制】不使用@import语法，如果有import需求，使用less的import
* 【建议】css缩写规范
    * hd  : header
    * ft  : footer
    * ma  : main
    * wp  : wrapper
    * inr : inner
    * bg  : background
    * nav : navigator
    * bt  : button
    * sd  : sidebar
    * lg  : logo
    * bnr : banner
    * ct  : content
    * tl  : title

