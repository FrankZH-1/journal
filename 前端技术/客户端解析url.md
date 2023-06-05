# 客户端解析url

在客户端解析 URL 可以使用 JavaScript 中的 `window.location` 对象。该对象包含有关当前 URL 的信息，如协议、主机、路径、查询字符串等等。

以下是使用 `window.location` 对象解析 URL 的示例代码：

```javascript
// 获取当前页面的 URL
var url = window.location.href;

// 获取当前页面的协议，如 "http" 或 "https"
var protocol = window.location.protocol;

// 获取当前页面的主机名和端口号，如 "example.com" 或 "example.com:8080"
var host = window.location.host;

// 获取当前页面的主机名，不包括端口号
var hostname = window.location.hostname;

// 获取当前页面的路径名，如 "/home/index.html"
var pathname = window.location.pathname;

// 获取当前页面的查询字符串，如 "?page=home&id=123"
var search = window.location.search;

// 解析查询字符串，将其转换为对象
var params = new URLSearchParams(search);
var page = params.get('page'); // 获取查询参数 "page" 的值
var id = params.get('id'); // 获取查询参数 "id" 的值
```

注意，`URLSearchParams` 对象是一个新的 API，如果需要在旧版浏览器中使用它，需要添加 polyfill。