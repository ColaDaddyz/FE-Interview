# HTTP 相关
* 为什么传统上利用多个域名来提供网站资源会更有效？
	一个域名有资源限制

* 请尽可能完整得描述从输入 URL 到整个网页加载完毕及显示在屏幕上的整个流程。
	> 	输入地址
		浏览器查找域名的 IP 地址
		这一步包括 DNS 具体的查找过程，包括：浏览器缓存->系统缓存->路由器缓存...
		浏览器向 web 服务器发送一个 HTTP 请求
		服务器的永久重定向响应（从 http://example.com 到 http://www.example.com）
		浏览器跟踪重定向地址
		服务器处理请求
		服务器返回一个 HTTP 响应
		浏览器显示 HTML
		浏览器发送请求获取嵌入在 HTML 中的资源（如图片、音频、视频、CSS、JS等等）
		浏览器发送异步请求

* Long-Polling、Websockets 和 Server-Sent Event 之间有什么区别？

* 请描述以下 request 和 response headers：
  * Diff. between Expires, Date, Age and If-Modified-...
  http://louiszhai.github.io/2017/04/07/http-cache/
  
  * Do Not Track
  * Cache-Control
  
  * Transfer-Encoding
  
  		> 传输编码
  			bigpipe 注意ng的缓冲区 
 * ETag
 
  -  X-Frame-Options
  
  		> X-Frame-Options 有三个值:
		DENY 表示该页面不允许在 frame 中展示，即便是在相同域名的页面中嵌套也不允许。
		SAMEORIGIN 表示该页面可以在相同域名页面的 frame 中展示。
      ALLOW-FROM uri 表示该页面可以在指定来源的 frame 中展示。
		换一句话说，如果设置为 DENY，不光在别人的网站 frame 嵌入时会无法加载，在同域名页面中同样会无法加载。另一方面，如果设置为 SAMEORIGIN，那么页面就可以在同域名页面的 frame 中嵌套。
* 什么是 HTTP method？请罗列出你所知道的所有 HTTP method，并给出解释。

* 301 和 302 区别
	用户没什么影响，影响seo

* HTTP2
https://developers.google.com/web/fundamentals/performance/http2/?hl=zh-cn

* HTTPS 
http://blog.csdn.net/small_dong_/article/details/52534738
对称+非对称
http://blog.jobbole.com/105405/

