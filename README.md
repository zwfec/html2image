**html2image **
----------------------------------------------------

文章: http://www.oschina.net/question/1027544_2141798
原始git：https://github.com/niklasvh/html2canvas

## 特殊说明:
0. demo演示请在具体的web 访问环境, 否则如果html中有图片时, 无法正常生成图片.
1. 具体使用请参考 demo
2. 主要解决二维码生成图片后无法识别的问题
```js
    var qr_url = 'http://www.updateweb.cn';
    $(".J_qr").qrcode({
        render: "canvas", width: 88, height: 88, text: qr_url, typeNumber: -1, correctLevel: 1
    });
    注意: 这里的 typeNumber: -1, correctLevel: 1
```
3. 解决取图时html 偏移的问题:
```js
var offset_top = 0;         // 请根据实际情况自定义 取值
var offset_left = 0;        // 请根据实际情况自定义 取值
var width = shareContent.offsetWidth + offset_left;  // 获取(原生）dom 宽度
var height = shareContent.offsetHeight + offset_top; // 获取(原生）dom 高
```
