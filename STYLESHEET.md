#样式文件开发规范

####文件命名规范
####选择器命名规范

* 【建议】css文件最外层选择器建议使用class
    * 【强制】common模块下的通用css：g-xxx
    * 【强制】模块下css：m(module)-xxx(模块名)-xxx
    * 【强制】组件下css：w(widget)-xxx(组件名)-xxx

####代码书写

* 【强制】杜绝!important
* 【建议】单个文件内选择器层级不超过4级
* 【强制】禁止在css中单独设置@charset
* 【强制】不使用@import语法，如果有import需求，使用less的import
* 【建议】css缩写规范
```
1)  hd  : header
2)  ft  : footer
3)  ma  : main
4)  wp  : wrapper
5)  inr : inner
6)  bg  : background
7)  nav : navigator
8)  bt  : button
9)  sd  : sidebar
10) lg  : logo
11) bnr : banner
12) ct  : content
13) tl  : title
```

