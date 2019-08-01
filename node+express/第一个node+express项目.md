# node-express-mock项目创建
  1、点击File，在弹出菜单中点击New Project，打开New Project界面。如下图1所示在New Project界面中选择Node.js Express App，修改Location名称，
  点击右下角Create。此时会弹出一个正在构建加载界面。当创建完成之后，加载界面消失，创建app成功。<br>
 ![Image Text](https://raw.githubusercontent.com/longlyboyhe/node-express-mock/master/public/images/1.png)<br>
                 图1<br>
2、App创建成功后整个项目结构如下图2所示。<br>
 ![Image Text](https://raw.githubusercontent.com/longlyboyhe/node-express-mock/master/public/images/2.png)<br>
                 图2<br>
其中bin中存在www文件，主要作用是启动Server服务，监听Server端口。<br>
node_modules中主要是依赖model类库。<br>
public中公共的图片、javascript和样式文件。<br>
views中存在页面相关。<br>
routes中存放路由相关js<br>

3、点击绿色的小三角如图3或正在命令行中输入npm run start命令，就可以启动项目。图4表面项目启动成功。<br>
 ![Image Text](https://raw.githubusercontent.com/longlyboyhe/node-express-mock/master/public/images/3.png)<br>
                          图3<br>

 ![Image Text](https://raw.githubusercontent.com/longlyboyhe/node-express-mock/master/public/images/4.png)<br>
                                   图4<br>
当项目启动成功后首先进到www.js中，引入需要的依赖包，并且监听3000端口。http.createServer(app)主要启动并创建Server。
这时在浏览器中输入localhost：3000，就可以打开界面了。如下图所示。<br>
![Image Text](https://raw.githubusercontent.com/longlyboyhe/node-express-mock/master/public/images/5.png)<br>
                          图5 <br>
连接成后的控制台输出如下所示。<br>
![Image Text](https://raw.githubusercontent.com/longlyboyhe/node-express-mock/master/public/images/6.png)<br>
![Image Text](https://raw.githubusercontent.com/longlyboyhe/node-express-mock/master/public/images/7.png)<br>
![Image Text](https://raw.githubusercontent.com/longlyboyhe/node-express-mock/master/public/images/8.png)<br>
![Image Text](https://raw.githubusercontent.com/longlyboyhe/node-express-mock/master/public/images/9.png)<br>
 

 
