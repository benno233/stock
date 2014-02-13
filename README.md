功能：

1. 股票页面聊天室功能：

   a. 聊天室以股票为单位，同一个用户可以进入多个股票的聊天室进行聊天 

   b. 聊天记录可以设置缓存数量，默认为20条，如果超过20条会存储到数据库中,当聊天室中没有用户也会将聊天内容存入数据库中

   聊天室代码：
   https://github.com/tangguangyao/stock/blob/master/models/socket.js


2. 微博类似的话题，评论，回复，转发功能，前端使用angularjs绑定实现

3. 页面实时交互，包括关注股票，关注用户功能

4. 股票页面能查看讨论这个股票的话题

5. 个人页面能查看我关注的用户的话题，关注股票的相关话题，我的话题，@我的话题

6. 加入grunt管理代码，引入uglify压缩代码，jshint检测代码规范，watch监听代码变化

7. 使用mocha检测后端代码
   检测代码在test中
   总结mocha单元测试经验
   http://hi.baidu.com/tang_guangyao/item/302a9d1a9976c06ae65e0643

8. 加入async流程控制，对于需要多次回调查询数据库的进行重构

9. 尝试bigpige，首页利用bigpipe，加载热门股票和热门用户，并且和angular结合使用

10. 使用外网免费数据库https://app.mongohq.com

11. 跨域请求的雪球网具体股票数据

12. 增加redis插件尝试（需要安装redis客户端http://redis.io/，推荐一个redis管理工具mac和win都可以使用http://redisdesktop.com/ ），首页点击我的评论，对我的评论加上redis处理，如果有缓存加载缓存内容，如果有缓存，但是在首页评论过，则去数据库取数据并且更新缓存


更新说明：因为股票具体数据是跨域请求的雪球网接口，雪球接口的参数会定时改变，所以对接口参数处理了一下，放入views的top.ejs文件中。