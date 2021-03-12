<template>
  <div>
    <h1>{{ msg }}</h1>
    <button v-on:click="drawRect">Test</button>
    <canvas id="canvas"></canvas>
  </div>
</template>

<script lang="ts">
import {onMounted} from "vue";
export default {
  name: 'Canvas',
  props: {
    msg: String
  },
  setup () {
    onMounted(() => {
      console.log("Mounted");
    })
  },
  methods: {
    drawRect() {
      console.log("Draw");  
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
