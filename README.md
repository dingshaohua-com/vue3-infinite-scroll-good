# vue3-infinite-scroll-good
## 简介
vue-infinite-scroll的vue3版本
所有用法和`vue-infinite-scroll`一致。   
其代码也是基于它做了简单修改，并修复了一些bug，比如无限加载或者下来会请求两次等问题。

## 示例
预览效果：[点击此处](https://dshvv.github.io/vue3-infinite-scroll-good/)   
示例源码：在根目录下的example中   
![preview](https://github.com/dshvv/vue3-infinite-scroll-good/blob/main/preview.gif)

## 安装
```shell
yarn add vue3-infinite-scroll-good
```

## 使用
```javascript
// 全局注册 mian.js
import infiniteScroll from 'vue3-infinite-scroll-good'
createApp(App).use(infiniteScroll).mount('#app');
```
```javascript
// 组件使用
<div v-infinite-scroll="loadMore" infinite-scroll-disabled="busy" infinite-scroll-distance="10">
  ...
</div>
var count = 0;

new Vue({
  el: '#app',
  data: {
    data: [],
    busy: false
  },
  methods: {
    loadMore: function() {
      this.busy = true;

      setTimeout(() => {
        for (var i = 0, j = 10; i < j; i++) {
          this.data.push({ name: count++ });
        }
        this.busy = false;
      }, 1000);
    }
  }
});
```

## 其他
喜欢就给个star      
百度`甲乙丙丁少`