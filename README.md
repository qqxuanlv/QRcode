
# QRcode

载入 JavaScript 文件
<script src="qrcode.js"></script>

DOM 结构
<div id="qrcode"></div>

调用

// 简单方式
new QRCode(document.getElementById('qrcode'), 'your content');

// 设置参数方式
var qrcode = new QRCode('qrcode', {
  text: 'your content',
  width: 256,
  height: 256,
  colorDark : '#000000',
  colorLight : '#ffffff',
  correctLevel : QRCode.CorrectLevel.H
});

// 使用 API
qrcode.clear();
qrcode.makeCode('new content');

参数说明
new QRCode(element, option)

名称      说明
element		显示二维码的元素或该元素的 ID
option		参数配置

option 参数说明
名称	默认值	说明
width	256	图像宽度
height	256	图像高度
typeNumber	4	
colorDark	"#000000"	前景色
colorLight	"#ffffff"	背景色
correctLevel	QRCode.CorrectLevel.L	容错级别，可设置为：
QRCode.CorrectLevel.L
QRCode.CorrectLevel.M
QRCode.CorrectLevel.Q
QRCode.CorrectLevel.H

API 接口
名称	说明
makeCode(text)	设置二维码内容
clear()	清除二维码。（仅在不支持 Canvas 的浏览器下有效）
