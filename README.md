# cors 跨域请求
### 运用方式
1. 更改本地hosts,映射本地访问 (Mac用sudo方式更改,windows用管理员运行记事本打开hosts更改)
> 127.0.0.1 cheche.com

> 127.0.0.1 duowan.com
2. 使用nodejs执行index.js,监听80端口 (Mac用sudo方式更改80端口,windows用管理员运行gitbush更改80端口),并且添加响应头`response.setHeader('Access-Control-Allow-Origin','http://duowan.com')`,`response.setHeader('Access-Control-Allow-Method','get,post,head')`让duowan.com获得跨域请求权限
3. 访问[http://cheche.com/cheche](http://cheche.com/cheche),发送AJAX请求[http://cheche.com/cheche_prototype.JSON](http://cheche.com/cheche_prototype.JSON)
4. 访问[http://duowan.com/duowan](http://duowan.com/duowan),发送AJAX请求[http://cheche.com/cheche_prototype.JSON](http://cheche.com/cheche_prototype.JSON),这样实现http://duowan.com对http://cheche.com跨域请求
