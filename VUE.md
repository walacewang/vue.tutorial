# VUE

* ## vue usage.

1. 大括号
```html
{{message}}
```
2. [v-bind]方式
```html
<span v-bind:title="message">example</span>
```
3. [v-if]指令
```html
<p v-if="seen">display</p>
```
>如果是多条语句时，使用<templete>,也可以组合使用else
```html
<template v-if="ok">
  <h1>Beijing</h1>
  <p>Welcome to Beijing.</p>
</template>
<template v-else>
  <h1>Shanghai</h1>
  <p>Welcome to Shanghai.</p>
</template>
```
4. [v-for]循环
```html
  <ol>
    <li v-for="todo in todos">
      {{ todo.text }}
    </li>
  </ol>
```
5. 事件绑定
```html
<div id="app-5">
  <p>{{ message }}</p>
  <button v-on:click="reverseMessage">逆转消息</button>
</div>
```
```javascript
var app5 = new Vue({
  el: '#app-5',
  data: {
    message: 'Hello Vue.js!'
  },
  methods: {
    reverseMessage: function () {
      this.message = this.message.split('').reverse().join('')
    }
  }
})
```
6. 数据双向绑定
```html
<div id="app-6">
  <p>{{ message }}</p>
  <input v-model="message">
</div>
```
```javascript
var app6 = new Vue({
  el: '#app-6',
  data: {
    message: 'Hello Vue!'
  }
})
```
