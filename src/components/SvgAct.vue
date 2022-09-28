<template>
  <div class="svg_all">
    <div class="svg_div">
      <Icon class="eye" icon="emoticon" :style="{ color: hairColor }" />
      <Icon class="eye" icon="emoticon" :style="{ color: '#fcff4d' }" />
    </div>

    <color-picker :value="hairColor" @change="changeColor"></color-picker>
  </div>
</template>

<script setup lang="ts">
// import colorPicker from 'vcolorpicker'
import ColorPicker from 'colorpicker-v3'
import { ref } from 'vue'

import Icon from '@/components/IconAct.vue'

const hairColor = ref('#b74dff')
const breadColor = ref('#fcff4d')

function changeColor(e) {
  console.log('e', e)
  hairColor.value = e.hex
}
</script>

<style>
@import 'colorpicker-v3/dist/style.css';

.svg_all {
  display: flex;
  flex-wrap: wrap;
  max-width: 31rem;
}

.svg_div {
  /* flex: 1; */
  position: relative;
  width: 15em;
  height: 15em;
  border: 1px solid slateblue;
}

.head {
  position: absolute;
  top: 0;
  left: 0;
}
</style>
