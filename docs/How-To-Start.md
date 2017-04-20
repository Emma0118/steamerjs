# 如何开始 —— 使用 steamerjs 安装与更新

## 安装 steamerjs 和脚手架管理插件

* [steamerjs](https://github.com/SteamerTeam/steamerjs)
* [steamer-plugin-kit](https://github.com/SteamerTeam/steamer-plugin-kit)

```javascript
npm i -g steamerjs steamer-plugin-kit
```

## 安装你喜欢的脚手架

```javascript
npm i -g steamer-simple steamer-react steamer-vue
```

## 本地部署脚手架

```javascript
steamer kit
// 然后选择你喜欢的脚手架
? which starterkit do you like:  (Use arrow keys)
❯ react
  simple
  vue
```

## 更新脚手架
```javascript
npm update -g steamer-simple steamer-react steamer-vue

// 进入你的项目目录
cd project

steamer kit --update
```
更新完毕，为将 `tools`，`package.json` `README.md` 做备份，其它内容会进行覆盖。