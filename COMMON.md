#各类型代码开发规范

### 样式表文件

* 【强制】CSS编码规范遵循公司整体[《CSS编码规范》](http://styleguide.baidu.com/style/css/index.html)

* 【建议】通用css文件命名建议：

    ```javascript
    .
    ├── src         //源文件目录
        ├── css         //css 样式文件目录
            ├── reset.css       //通用样式重置
            ├── tools.css       //通用工具类css（clearfix, wordwrap, ...）
            ├── layout.css      //通用布局类css
            ├── grid.css        //栅格化 css
    ```

* 【建议】css最外层选择器建议使用类选择器，最外层class命名建议：
    * common模块下的通用css：g-xxx
    * 模块下css：m(module)-xxx(模块名)-xxx
    * 组件下css：w(widget)-xxx(组件名)-xxx
* 【建议】不使用@import语法，如果有import需求，使用less的import
* 【强制】伪元素选择器使用`"::"`，伪类选择器使用`":"`，示例：

    ```css
    /*伪元素*/
    p::after{
        content: " ";
    }
    /*
        主要伪元素选择器：
        ::after, ::before, ::first-letter, ::first-line, ::selection
    */
    
    /*伪类*/
    a:hover{
        color: #000;
    }
    /*
        主要伪类选择器：
        :active, :checked, :disabled, :empty, :enabled, :first-child, :first-of-type, :focus, 
        :hover, :in-range, :invalid, :lang(language), :last-child, :last-of-type, :link, :not(selector),
        :nth-child(n), :nth-last-child(n), :nth-last-of-type(n), :nth-of-type(n), :only-of-type, :only-child,
        :optional, :out-of-range, :read-only, :read-write, :required, :root, :target, :valid, :visited
    */
    
    ```

* 【建议】css类选择器缩写建议
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
* 【建议】响应式布局样式文件书写建议：
    ```javascript
    .
    ├── less                 //样式文件目录
        ├── home.less                   //默认页面最小宽度样式
        ├── home_width_l_1280.less      //浏览器宽度 <= 1280px && > min 样式
        ├── home_width_l_1680.less      //浏览器宽度 <= 1600px && > 1280 样式
        ├── home_width_l_1920.less      //浏览器宽度 <= 1920px && > 1600 样式
        ├── ...
    ```
    * less

###JavaScript文件


