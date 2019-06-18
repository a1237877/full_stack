大前端全栈开发思路

在前端vue 项目目录下 建一个server 用来做mvc就好了
- 前后端分离
后端负责提供/api  在server目录下
前端在src/

API 服务
后端就负责 API 服务

- 后端在3000端口 未来等着ngnix 将80端口指向3000
/api API服务等着前端服务   / vue打包好的dist目录 index.html readFile 返回
- 前端一般在8080端口 负责 vue-router vuex axios
- 前后端连调  api 数据 -> vue 组件的data  
- 跨域 前端面试最重要的问题
  domain 域名
  端口cross domain
  前端不允许  安全问题
  前端考虑 页面上显示的安全
  后端考虑 

  book.douban.com
  www.douban.com
  subdomain:domain:port 都一样
  js 同源机制 相同的源是值得依赖的
  前后端 8080：3000 跨域
  不跨 fetch('/api/user/login) 404
  3000 /api/ 提供一个proxy 代理
  匹配/api/
  target：http://localhost:3000,
  changeOrigin:true
  发出去的请求也不跨域