# SPA Development 多页开发

## 新建页面
在 `tools/template` 目录下都有一个默认的模板 `index`。开发者可以通过以下命令新建页面。通过命令，会在 `src/page` 目录下基于 `index` 模板，生成 detail 页面的所需资源。

```javascript
npm run tpl --tpl=index --path=detail
或
npm run tpl -t=index -p=detail
```


## 创建模板

## 对指定 chunk 进行编译
有的时候，你开只开发其中一个页面或其中一个chunk，但你将所有文件一起编译，会较为浪费时间，你可通过以下参数来选择性编译，这个命令只对 detail 和 index 两个 chunk (实际是 js/detail 和 js/index 2 个 chunk, 这里兼容了简写) 进行编译:

```javascript
npm run dist --entry=detail,index
```