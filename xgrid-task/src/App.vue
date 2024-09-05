<script setup>
import {ref , watchEffect} from 'vue'

const hours = ref(0)
const minutes = ref(0)
const seconds = ref(0)


watchEffect(()=>{
  if(minutes.value===59){
    hours.value = hours.value++
    minutes.value = 0
  }
  // if(seconds.value===59)
})


</script>

<template>
  <div class="flex items-center justify-center">
    <div class="w-48 h-48 rounded-md border-black border-2 mt-3 flex items-center " >
        hours: {{ hours }}
        minutes: {{minutes}}
        seconds: {{seconds}}
    </div>
  </div>

</template>

<style scoped>
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
