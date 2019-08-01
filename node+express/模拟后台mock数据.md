# 模拟后台mock数据
## 前提
### 1、Web应用前后端(台)分离:
   后台向前台提供API接口,只负责数据的提供和计算，而完全不处理展现
前台通过Http(Ajax)请求获取数据,　在浏览器端动态构建界面显示数据

### 2、设计JSON数据结构

### 3、利用Node+express提供模拟数据
优点：可以在浏览器端访问
缺点：如果是打包发布就无法访问模拟数据, 只能是测试时使用

与以往的自己模拟的假数据不同，mockjs可以带给我们的是：在后台接口未开发完成之前模拟数据，并返回，完成前台的交互；在后台数据完成之后，你所做的只是去掉mockjs：停止拦截真实的ajax，仅此而已。

具体操作
步骤一.将 data.json 文件拷贝到 sellapp 目录下（与 index.html 同级）

模拟的数据请求是从 data.json 中读取数据，接下来就来编写这些接口。

步骤二.在 webpack.dev.conf.js 中添加以下代码：

此次开发过程需要去本地数据地址进行请求，而原版配置在 dev-server.js 中，新版 vue-webpack-template 已经删除 dev-server.js，改用webpack.dev.conf.js代替，所以配置本地访问在 webpack.dev.conf.js 里配置即可。这里使用 express 框架去写一个 nodeserver，也可以用 express-router 来编写这些接口请求。

#### 1）先获取数据：获取data.json中的数据，再分别将商家，商品，评论数据写入相应变量中

#### 2）编写路由及相应接口

解析：调用 get 方法，传入 seller 接口，发送请求，服务端接受请求，返回给客户端一个json类型的数据（包括 errno 及数据），其中 errno 是开发规范所有，当其值为0时，表示返回的数据正常，当遇到一些比如权限限制时，errno 可能不为0，具体值是由也业务方规定的。因为本次项目使用的是模拟数据，所以 errno 一定为0。

#### 3）运行

npm run dev，启动后输入http://localhost:8080/api/seller，如果数据正常显示，则数据能正常返回

参考原文：https://www.cnblogs.com/enboke/p/vue.html

PS：

1.Google可以用 jsonview 插件将返回数据格式化

2.express相关语法：https://github.com/expressjs/express/blob/master/Readme.md

3.app.use和app.get的区别及解析：http://blog.csdn.net/wthfeng/article/details/53366169
