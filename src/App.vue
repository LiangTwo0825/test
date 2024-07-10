
<template>
  <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
    <button class="btn" @click="add">点击{{ state.data.num }}次</button>
  </div>
</template>
<script setup>
import { reactive } from 'vue';


const state = reactive({
  data: {
    num: 0
  }
})


const add = () => {
  state.data.num++

}

</script>

<style scoped>
div{
  display: flex;
  flex-direction: column;
}
.btn{
}
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
