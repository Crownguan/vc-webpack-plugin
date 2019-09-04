# vconsole-webpack-plugin
webpack plugin for [vConsole](https://github.com/WechatFE/vConsole)

帮助开发者在移动端进行调试，本插件是在 [vConsole](https://github.com/WechatFE/vConsole) 的基础上封装的 `webpack` 插件，通过 `webpack` 配置即可自动添加 `vConsole` 调试功能，方便实用。

## 安装

```bash
npm install vconsole-webpack-plugin --save-dev
```

## 使用

`webpack.conf.js` 文件配置里增加以下插件配置即可

```js
// 引入插件
var vConsolePlugin = require('vconsole-webpack-plugin'); 

module.exports = {
    ...

    plugins: [
        new vConsolePlugin(),
        ...
    ]
    ...
}
```

当然，有时候一些页面想临时添加 `vconsole` 来调试一下，可以直接使用：

```htmls
<script src="http://wechatfe.github.io/vconsole/lib/vconsole.min.js?v=3.2.0"></script>
<script>
	window.vConsole = new window.VConsole();
</script>
```
