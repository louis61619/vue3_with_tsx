<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>{{ age }}</h2>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

// 需要告訴ts這個物件是不可變的
const Proptyps = {
  msg: String,
  age: {
    type: Number,
    required: true,
  },
} as const

export default defineComponent({
  name: 'HelloWorld',
  props: Proptyps,
  mounted() {
    this.age
  },
})
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
