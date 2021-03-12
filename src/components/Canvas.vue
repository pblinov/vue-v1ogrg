<template>
  <div>
    <h1>{{ msg }}</h1>
    <button v-on:click="drawRect">Test</button>
    <canvas ref="canvas"></canvas>
  </div>
</template>

<script lang="ts">
import {ref, onMounted} from "vue";
export default {
  name: 'Canvas',
  props: {
    msg: String
  },
  setup () {
    let canvas = ref("canvas")
    onMounted(() => {
      let width = canvas.getAttribute('width');
      console.log("Mounted" + width);
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
