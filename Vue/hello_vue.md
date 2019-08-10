# hello vue

## 特点
- 响应式
    可以在 JavaScript 控制台实时修改变量
    
## hello vue

```html
<!-- 导入Vue -->
<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>

<div id="app">
  {{ message }}    <!-- 显示文本 -->
</div>
```

```js
var app = new Vue({
  el: '#app',
  data: {
    message: 'Hello Vue!'
  }
})
```

## 与DOM属性绑定
```html
<!-- 将‘title’属性绑定为‘message’变量 -->
<div id='hid' v-bind:title="message">    
        鼠标悬停几秒钟查看此处动态绑定的提示信息！
</div>
```
```js
var hid = new Vue({
  el: '#hid',
  data:{
      message: '页面加载于：'+ new Date().toLocaleString()
  }
})
```

## 条件判断
```html
<!-- 添加条件判断 -->
<div id='hid' v-if="condition">
  隐藏
</div>
```
```js
var hid = new Vue({
	el: '#hid',
	data:{
		condition: false
	}
})
```

## 循环语句
```html
<!-- 选中父元素 -->
<ol id='for_each' >
    <!-- 循环生成列表 -->
	<li v-for="(item, index) in items" :key="index">
		{{item.text}}
	</li>
</ol>
```
```js
var for_each = new Vue({
  el: '#for_each',
  data: {
    items: [
      {text: '学习 JavaScript'},
      {text: '学习 Vue'},
      {text: '整个牛项目'}
    ]
  }
})
```
```js
// 添加新项
for_each.items.push({text: '新项目'})
```

## 事件监听
```html
<div id="rev">
    <p>{{message}}</p>
    <!-- v-on事件监听 -->
    <button v-on:click="reverseMessage">reverse</button>
</div>
```
```js
var rev = new Vue({
    el: '#rev',
    data: {
        message: 'test text'
    },
    methods: {
        reverseMessage: function(){
	    // str - list - list - str, str没有reverse方法
            this.message = this.message.split('').reverse().join('')
        }
    }
})
```