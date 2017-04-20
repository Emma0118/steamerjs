# steamer-plugin-example

steamer plugin 例子

## 如何写一个 steamerjs 插件

* 创建一个函数

```javascript
steamer example -c config.js
// 或
steamer example --config config.js
```

当上述命令启动时，一个命令参数会传入函数中。更多相关参数的文档，请参考 [yargs](https://github.com/yargs/yargs).

```javascript
function ExamplePlugin(argv) {
	this.argv = argv;
}
```

* 创建 `init` 函数

为插件创建 `init` prototype 函数， 因为命令在启动时会自动调用此函数。

```javascript
ExamplePlugin.prototype.init = function() {
	console.log(this.argv);
};

module.exports = ExamplePlugin;
```

* Specify a main file and a bin file in package.json

```javascript
"main": "index.js"
```

* 创建 `help` 函数

使用下面命令时，会自动调用 `help` 函数，主要用于输出插件帮助文档。

```
steamer example -h
// 或
steamer example --help
```

## `Util` 库

开发插件时，常常需要一些 `Util` 函数，帮助你快速开发，`Steamer` 提供以下 `Util` 库：

* [steamer-pluginutils](https://github.com/SteamerTeam/steamer-pluginutils)

## 开发

```javascript
// 将你的插件传至全局路径，那你就可以直接使用 `steamer example`
npm link

// 当你完成开发，可以 `unlink` 你的插件
npm unlink

```
