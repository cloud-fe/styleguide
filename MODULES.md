#模块划分&命名

* 【强制】模块必须以功能维度进行划分
```
例如：

XXX平台
├── 主站            //home 模块
├── 个人后台        //console 模块
    ├── 后台配置        //console 模块 —— backend
    ├── 管理页          //console 模块 —— management
    ├── ...
├── 消息中心        //message 模块
    ├── 消息列表页      //message 模块 —— list
    ├── 消息详情页      //message 模块 —— detail
├── 用户中心        //user 模块
    ├── 用户详情页      //user 模块 —— detail
    ├── 用户注册页      //user 模块 —— register
    ├── 资质状态页      //user 模块 —— status
├── ...
```
* 【强制】同级模块必须有通用模块，通用模块命名：common
```
例如：
xxx
├── common
├── home
├── console
├── ...
