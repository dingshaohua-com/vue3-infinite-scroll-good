# vue3-infinite-scroll-good
## 简介 (introduce)
vue-infinite-scroll的vue3版本,所有用法和`vue-infinite-scroll`一致。   
vue3 version of vue-infinite-scroll. All usages are consistent with `vue-infinite-scroll`   

其代码也是基于它做了简单修改，并修复了一些bug，比如重复两次请求等问题。   
The code is also based on it, made simple modifications, and fixed some bugs, such as repeated requests twice.   


## 示例 (Example)
预览效果：[Demo](https://dshvv.github.io/vue3-infinite-scroll-good/)   
preview：[Demo](https://dshvv.github.io/vue3-infinite-scroll-good/)   

示例源码：在根目录下的example中   
Example source code: in example under the root directory   
![preview](https://github.com/dshvv/vue3-infinite-scroll-good/blob/main/preview.gif)

## 安装 (install)
```shell
yarn add vue3-infinite-scroll-good
```

## 使用 (use)
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

## 其他(other)
喜欢就给个star      
Give a star if you like   

百度`甲乙丙丁少`   
Google`甲乙丙丁少`
