# SPA Development 多页开发

## 新建页面
在 `tools/template` 目录下都有一个默认的模板 `index`。开发者可以通过以下命令新建页面。通过命令，会在 `src/page` 目录下基于 `index` 模板，生成 detail 页面的所需资源。

```javascript
npm run tpl --tpl=index --path=detail
或
npm run tpl -t=index -p=detail
```


## 创建模板

你可以在 `tools/template` 目录下创建你的模板。模板创建可以参考已经存在的模板，默认模板是 `index` 目录。

模板的生成主要由 `tools/template.js` 脚本处理，`steamer-webpack-utils` 的 `walkAndReplace` 方法，会对模板里的的指定后缀文件进行扫描，如果找到像 `<% title %>` 这样的占位符，会将你想要替换的字符串进行替换。如：

```javascript
npm run tpl --tpl=index --path=detail

// <% title %> 会被替换成 detail

```


## 对指定 chunk 进行编译
有的时候，你开只开发其中一个页面或其中一个chunk，但你将所有文件一起编译，会较为浪费时间，你可通过以下参数来选择性编译，这个命令只对 detail 和 index 两个 chunk (实际是 js/detail 和 js/index 2 个 chunk, 这里兼容了简写) 进行编译:

```javascript
npm run dist --entry=detail,index
```