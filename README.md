###目录


sign.html - 手写签名板
pop.html  - 泡泡动画




###<canvas>

该标签定义图形，只是图形容器，使用脚本来绘制图形

context = canvas . getContext(contextId)
方法返回一个指定contextId的上下文对象，如果指定的id不被支持，则返回null，当前唯一被强制必须支持的是“2d”，也许在将来会有“3d”，注意，指定的id是大小写敏感的。


此函数，返回一张使用canvas绘制的图片，返回值符合data:URL格式，格式如下：
url = canvas . toDataURL( [ type, ... ])
规范规定，在未指定返回图片类型时，返回的图片格式必须为PNG格式，如果canvas没有任何像素，则返回值为：“data:,”，这是最短的data:URL，在text/plain资源中表现为空字符串。type的可以在image/png，image/jpeg,image/svg+xml等 MIME类型中选择。如果是image/jpeg，可以有第二个参数，如果第二个参数的值在0-1之间，则表示JPEG的质量等级，否则使用浏览器内置默认质量等级。
下面的代码可以从ID为codeex的canvas中取得绘制内容，并作为DataURL传递给img元素，并显示。
var canvas = document.getElementById('codeex');
var url = canvas.toDataURL();
//id为myimg的图片元素
myimg.src = url;