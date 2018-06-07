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
<template v-if="city==='B'">
  <h1>Beijing</h1>
  <p>Welcome to Beijing.</p>
</template>
<template v-else-if="city === 'S'">
  <h1>Shanghai</h1>
  <p>Welcome to Shanghai.</p>
</template>
<template v-else>
  <h1>unknown</h1>
  <p>Welcome</p>
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
  
* ## 注意事项

1. ### 由于 JavaScript 的限制，Vue 不能检测以下变动的数组：
> [注意](https://cn.vuejs.org/v2/guide/list.html#%E5%AF%B9%E8%B1%A1%E6%9B%B4%E6%94%B9%E6%A3%80%E6%B5%8B%E6%B3%A8%E6%84%8F%E4%BA%8B%E9%A1%B9)

* 当你利用索引直接设置一个项时，例如：vm.items[indexOfItem] = newValue
* 当你修改数组的长度时，例如：vm.items.length = newLength

```html
vm.$set(vm.items, indexOfItem, newValue)
```
```html
vm.items.splice(newLength)
```
2. ### 事件修饰符
> [注意](https://cn.vuejs.org/v2/guide/events.html#%E4%BA%8B%E4%BB%B6%E4%BF%AE%E9%A5%B0%E7%AC%A6)
