# attmall

[![ver-image]][ver-url]

测试模块

## Installation
这是一个可以通过 [npm registry](https://www.npmjs.com/) 使用的 [Node.js](https://nodejs.org/en/) 模块。
安装是使用[`npm install` 命令](https://docs.npmjs.com/getting-started/installing-npm-packages-locally): 

```sh
$ npm install attmall
```

## API

```js
var attmall = require('attmall')
```


### attmall.say(string)

返回欢迎信息


```js
// 返回“开发者您好，欢迎访问ATT商城”
attmall.say('开发者')
```

## Examples

### 页面上显示“用户您好，欢迎访问ATT商城”

```js
var http=require('http');
var attmall=require('attmall');

http.createServer(function(req, res){
    res.setHeader('Content-Type', 'text/html')
    res.end(attmall.say('用户'));
}).listen(8888);

console.log('Server running at http://127.0.0.1:8888/');
```

## License

[MIT](http://opensource.org/licenses/MIT)

[ver-image]: https://badgen.net/badge/version/v1.0.11/blue
[ver-url]: https://npmjs.org/package/attmall
