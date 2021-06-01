### HTTP服务器

#### 1. 导入http库

```
var http = require('http')
```

####  2.绑定端口号，启动监听服务

```
server.on('request', function(req, res) {
}) // 监听
server.listen(3000,function(){
console.log('server start...')
})
```

#### 3. 路由匹配

```
server.on('request', function(req, res) {
var url = req.url
if (url === '/index'){
res.end('<p>index 主页</p>')
}else {
res.end('other')
}
})
```

#### 4. 添加响应头

```
res.setHeader(
'Content-Type','text/html;charset=utf-8'
)
```

- 常见的媒体格式类型
    - text/html ： HTML格式
    - text/plain ：纯文本格式
    - text/xml ： XML格式
    - image/gif ：gif图片格式
    - image/jpeg ：jpg图片格式
    - image/png：png图片格式
    - application/xhtml+xml ：XHTML格式
    - application/xml： XML数据格式
    - application/json： JSON数据格式
    - application/pdf：pdf格式
    - application/octet-stream ： 二进制流数据（如常见的文件下载）
    - multipart/form-data ： 需要在表单中进行文件上传时，就需要使用该格式

#### 5. 

