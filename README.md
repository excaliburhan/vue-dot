# vue-dot
一个...文字循环组件

## 安装

> npm install vue-dot --save

## 使用

### 全局组件

```
import vueDot from 'vue-dot'
Vue.use(vueDot)
```

### 局部组件

```
import { vueDot } from 'vue-dot'

new Vue({
  components: {
    vueDot
  },
  data () {
    return {
      number: 12,
    }
  }
})

<p>载入中<vue-dot></vue-dot></p>
```
