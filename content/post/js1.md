---
title: "Js对象基本用法"
date: 2020-07-14T21:32:28+08:00
draft: false
---

内容 1：声明对象的两种语法
内容 2：如何删除对象的属性
内容 3：如何查看对象的属性
内容 4：如何修改或增加对象的属性
内容 5：'name' in obj 和 obj.hasOwnProperty('name') 的区别

# 声明对象

`let obj = { 'name': 'frank', 'age': 18 }`

`let obj = new Object({'name': 'frank'})`

`console.log({ 'name': 'frank, 'age': 18 })`

- 键名是字符串，不是标识符，可以包含任意字符
- 引号可省略，省略之后就只能写标识符
- 就算引号省略了，键名也还是字符串（重要）
- 'key':value 即 '属性名'：属性值
- 可以用[]将属性名括起来，这样属性名可以是变量。不加 []的属性名会自动变成字符串，而加了的会当作变量求值。

# 增删改查

## 删除

- delete obj.xxx 或 delete obj['xxx']

  即可删除 obj 的 xxx 属性

- 'xxx' in obj === false

  含有属性名，但是值为 undefined

- 'xxx' in obj && obj.xxx === undefined

  注意 obj.xxx === undefined 不能断定 'xxx' 是否为 obj 的属性

## 查看

- 查看自身所有属性
  `Object.keys(obj)`
- 查看自身+共有属性
  `console.dir(obj)`
- 或者自己依次用 `Object.keys` 打印出 `obj.__proto__`
  判断一个属性是自身的还是共有的
  `obj.hasOwnProperty('toString')`
- 查看某一个属性

  中括号语法：`obj['key']`

  点语法：`obj.key`

- 写

### 直接赋值

```
let obj = {name: 'frank'} // name 是字符串
obj.name = 'frank' // name 是字符串
obj['name'] = 'frank'
obj[name] = 'frank' // 错，因 name 值不确定
obj['na'+'me'] = 'frank'
let key = 'name'; obj[key] = 'frank'
let key = 'name'; obj.key = 'frank' // 错,因为 obj.key 等价于 obj['key']
```

### 批量赋值

`Object.assign(obj, {age: 18, gender: 'man'})`

### 改变共有属性

修改或增加共有属性

```
let obj = {}, obj2 = {} // 共有 toString
obj.toString = 'xxx' //只会在改 obj 自身属性
obj2.toString //还是在原型上
```

修改原型上的属性

```
obj.__proto__.toString = 'xxx' // 不推荐用 __proto__
Object.prototype.toString = 'xxx'
```

修改隐藏属性

- 使用**proto**

```
let obj = {name:'frank'}
let obj2 = {name: 'jack'}
let common = {kind: 'human'}
obj.__proto__ = common
obj2.__proto__ = common

```

- 使用 create

```
let obj = Object.create(common)
obj.name = 'frank'
let obj2 = Object.create(common)
obj2.name = 'jack'
```

ES6 推荐使用 create

- ps：`'name' in obj`和`obj.hasOwnProperty('name')`的区别在于，前者判断 obj 含不含属性名'name'，后者判断 name 是不是 obj 自有的属性。
