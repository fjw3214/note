**目录:**
* [1XX系列](#1XX系列)
* [2XX系列: 成功](#2XX系列)
* [3XX系列: 重定向](#3XX系列)
* [4XX系列](#4XX系列)
* [5XX系列](#5XX系列)

**常见的状态码有1XX,2XX,3XX,4XX,5XX系列**
# 1XX系列
*  100，continue 继续：  
服务器仅接收到部分请求，并且服务器并没有拒绝该请求，客户端应该继续发送其余的请求。一般在发送post请求时，已发送了http header之后服务端将返回此信息，表示确认，之后发送具体参数信息。
* 101 Switching Protocols：  
服务器转换协议：服务器将遵从客户的请求转换到另外一种协议。
* 102: 由WebDAV（RFC 2518）：  
扩展的状态码，代表处理将被继续执行

# 2XX系列
* 200 OK：    
请求成功（其后是对GET和POST请求的应答文档。）
* 201 Created：  
请求成功并且服务器创建了新的资源
* 202 Accepted：  
供处理的请求已被接受，但尚未处理。
* 203 Non-authoritative Information：   
文档已经正常地返回，但一些应答头可能不正确，因为使用的是文档的拷贝。
* 204 No Content：  
若服务器拒绝对PUT、POST或者DELETE请求返回任何状态信息或表示，那么通常采用此响应代码。服务器也可以对GET请求返回此响应代码，这表明“客户端请求的资源存在，但其表示是空的”。注意与304("Not Modified")的区别。204常常用在Ajax应用里。服务器通过这个响应代码告诉客户端：客户端的输入已被接受，但客户端不应该改变任何UI元素
* 205 Reset Content：  
没有新文档。但浏览器应该重置它所显示的内容。用来强制浏览器清除表单输入内容。
* 206 Partial Content：  
客户发送了一个带有Range头的GET请求，服务器完成了它。

# 3XX系列
* 300 Multiple Choices：  
多重选择。链接列表。用户可以选择某链接到达目的地。最多允许五个地址。
* 301 Moved Permanently：  
所请求的页面已永久移动到新位置
* 302 Found：  
所请求的页面已经临时转移至新的url。
* 303 See Other：  
所请求的页面可在别的url下被找到，请求已经被处理，但服务器不是直接返回一个响应文档，而是返回一个响应文档的URI。
* 304 Not Modified：  
未按预期修改文档。客户端有缓冲的文档并发出了一个条件性的请求（一般是提供If-Modified-Since头表示客户只想比指定日期更新的文档）。服务器告诉客户，原来缓冲的文档还可以继续使用。
* 305 Use Proxy：  
客户请求的文档应该通过Location头所指明的代理服务器提取。
* 306 Unused：  
此代码被用于前一版本。目前已不再使用，但是代码依然被保留。
* 307 Temporary Redirect：  
被请求的页面已经临时移至新的url。
## 4XX系列
* 400 Bad Request：  
服务器未能理解请求。
* 401 Unauthorized：  
被请求的页面需要用户名和密码。
* 401.1：  
登录失败。
* 401.2：  
服务器配置导致登录失败。
* 401.3：  
由于 ACL 对资源的限制而未获得授权。
* 401.4：  
筛选器授权失败。
* 401.5：  
ISAPI/CGI 应用程序授权失败。
* 401.7：  
访问被 Web 服务器上的 URL 授权策略拒绝。这个错误代码为 IIS 6.0 所专用。
* 402 Payment Required：  
此代码尚无法使用。
* 403 Forbidden：  
对被请求页面的访问被禁止。
* 404 Not Found:  
服务器无法找到被请求的页面。
* 405 Method Not Allowed:  
请求中指定的方法不被允许。
* 406 Not Acceptable:  
服务器生成的响应无法被客户端所接受。
* 407 Proxy Authentication Required:  
用户必须首先使用代理服务器进行验证，这样请求才会被处理。
* 408 Request Timeout:  
请求超出了服务器的等待时间。
* 409 Conflict:  
由于冲突，请求无法被完成。
* 410 Gone:  
被请求的页面不可用。
* 411 Length Required:  
“Content-Length” 未被定义。如果无此内容，服务器不会接受请求。
* 412 Precondition Failed:  
请求中的前提条件被服务器评估为失败。
* 413 Request Entity Too Large:  
由于所请求的实体的太大，服务器不会接受请求。
* 414 Request-url Too Long:  
由于url太长，服务器不会接受请求。当post请求被转换为带有很长的查询信息的get请求时，就会发生这种情况。
* 415 Unsupported Media Type:  
由于媒介类型不被支持，服务器不会接受请求。
* 416 Requested Range Not Satisfiable:  
服务器不能满足客户在请求中指定的Range头。
* 417 Expectation Failed:  
执行失败。
* 423:  
锁定的错误。

## 5XX系列
* 500 Internal Server Error：  
请求未完成。服务器遇到不可预知的情况。
* 501 Not Implemented：  
请求未完成。服务器不支持所请求的功能。
* 502 Bad Gateway：  
请求未完成。服务器从上游服务器收到一个无效的响应。
* 503 Service Unavailable：  
请求未完成。服务器临时过载或宕机。
* 504 Gateway Timeout：  
网关超时。
* 505 HTTP Version Not Supported：  
服务器不支持请求中指明的HTTP协议版本


