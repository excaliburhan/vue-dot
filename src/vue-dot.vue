<template>
<span class="vue-dot">{{ dotText }}</span>
</template>

<script>
export default {
  name: 'vue-dot',
  props: {
    dot: {
      type: String,
      default: '.',
    },
    count: {
      type: Number,
      default: 3,
    },
    interval: {
      type: Number,
      default: 1000,
    },
  },
  data () {
    return {
      timer: null,
      index: 0, // 计数
    }
  },
  computed: {
    dotText () {
      let str = this.index % this.count + 1
      return ('.').repeat(str)
    },
  },

  mounted () {
    this.timer = setInterval(() => {
      this.index++
    }, this.interval)
  },
  beforeDestroy () {
    clearInterval(this.timer)
  },
}
</script>
