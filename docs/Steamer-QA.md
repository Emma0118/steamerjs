# Steamerjs 常见问题

## NODE_PATH的全局变量(若无报错，可不设置)
`steamerjs` 体系内，有不少需要调用 `NODE_PATH` 位置的，因此需要设置好此变量。如果无报错，但并无设置，也建议进行设置，这样可以让命令行启动的速度更快些。

`MacOS`

* 默认值为：`/usr/local/lib/node_modules`

```javascript
export PATH=$PATH: # 将 /usr/bin 追加到 PATH 变量中
export NODE_PATH="/usr/lib/node_modules;/usr/local/lib/node_modules" #指定 NODE_PATH 变量

```

`Windows`

* 32位默认值为：`C:\Program Files (x86)\nodejs\node_modules`
* 64位默认值为：`C:\Program Files\nodejs\node_modules`

```javascript
1. 鼠标右击计算机
2. 属性
3. 高级系统设置
4. 环境变量
5. 系统变量，设置NODE_PATH
```

注意，如果你的系统需要多个 `Node` 版本，共存，建议 `MacOS` 使用 [nvm](https://github.com/creationix/nvm)，`Windows` 使用 [nvm-windows](https://github.com/coreybutler/nvm-windows)。

选定主要版本后，再安装 `steamerjs` 及其它生态的相关插件或者脚手架。