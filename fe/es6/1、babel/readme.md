# 问题
## 正常安装使用流程
1. npm install --save-dev @babel/core
2. 根目录下配置文件.babelrc

```
 {
    "presets": [
      "@babel/env",
      "@babel/preset-react"
    ],
    "plugins": []
  }
```

3. npm install --save-dev @babel/preset-env
4. npm install --save-dev @babel/cli
5. 单个文件转码 npx babel example.js --out-file compiled.js
6. 整个目录转码:npx babel src --out-dir lib


## REPL指的是什么
> “读取-求值-输出”循环（英语：Read-Eval-Print Loop，简称REPL）是一个简单的，交互式的编程环境

## Babel相关问题
1、安装@babel /core时报错
```
No package.json found: Cannot audit a project without a package.json
```
是因为在当前项目中没有package.json，而没有的原因是该项目不是一个node模块，所以解决方案就是将当前的项目模块化
```
npm init
```

2. Babel编译时为什么用的是npx
	- npx是一种在npm中安装工具，也可以被单独的下载使用
	- 再也不需全局安装任何工具只需要npx <commang>
	- 任何command都通过npx在machine任何位置使用

``` 
	npx babel example.js
```
	



## 代码问题
	
1. 箭头函数
	- 箭头函数写代码拥有更加简洁的语法
	- 不会绑定this

```javascript
(parameters) => { statements }
//如果没有参数，那么可以进一步简化
() => { statements }
//如果只有一个参数，可以省略括号
parameters => { statements }
//如果返回值仅仅只有一个表达式(expression), 还可以省略大括号
parameters => expression
// 等价于:
function (parameters){
  return expression;
}
```
2. map的用法
	- 是数组方法
	- 返回值是处理后的数组
	- array.map(function(currentValue,index,arr), thisValue)

```javascript
let input=[1,2]
let arr=input.map(item=>item+2);
console.info(arr)
```