# 本地服务器的搭建

1.安装phpstudy  目的是运行mysql 绿灯亮表示mysql数据库软件启动成功
2.安装sqlyog  它是数据库mysql的图形化界面 相当于Mongodb中的compass
（运行它必须先启动phpstudy即必须先运行mysql）
3.找到数据库 mydb.sql文件
4.导入数据库
    1.在sqlyog中创建数据库 mydb
    2.导入数据库文件
5.启动node.js服务器  vue_api_server 服务器文件

路由导航==路由监听
 前置+后置+路由独享的守卫+组件内的守卫

路由跳转步骤：
 login.vuw
    1.登陆成功后将token做本地缓存
    2.实现编程式导航跳转
router.js
    1.使用路由拦截守卫
    2.判断是否式login 如果是==next()
    3.获取本地缓存
    4.判断token值不存在就跳回login 否则next()

路由导航守卫/路由拦截器===只要是路由地址发生变化就会触发
axios拦截器===只要是发送请求就会触发

左侧导航修复功能实现
1.设置属性显示高亮 active-text-color="#123456"
2.设置导航图标 data中定义一个对象
3.解决只显示一个展开栏  
    1.添加unique-opend属性
    2.设置index的属性值必须是唯一值而且是字符串
4.关闭动画和导航宽度的切换
    1.设置属性iscollapse=true 折叠 反之就是展开
    2.绑定点击事件来设置bool值
    3.设置侧边栏的宽度 ==判断iscollapse的值来进设置宽度的切换
    4.取消动画 :collapse-transition="false"
5.解决左侧菜单状态保持  高亮+展开
    1.设置属性 default-active='路由值'
    2.绑定点击事件
        1.将路由值做本地缓存
        2.将路由值赋值给data中的属性
    3.重新进入
        获取本地缓存 然后将值赋值给data中的属性
