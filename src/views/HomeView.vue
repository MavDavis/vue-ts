<template>
  <div class="home">
    <p>{{name}} - {{age}}years</p>
    <button @click="changename('cannot change to number')">changename</button>
    <button @click="changenage(78)">changAge</button>
</div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'HomeView',
  setup(){
const name = ref('string')
const age = ref(12)
return { name,age}
  },
  components: {
  },
  methods:{
changename(build:string){
this.name = build
},changenage(build:number){
this.age = build
}
  }
});
</script>
