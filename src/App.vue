<template lang="pug">
  #app(:style="{backgroundColor: bgColor}")
    GitHubRibbon
    VueProductSpinner(:imgs="imgs")
    .color-selection
      .color(v-for="color in colors", 
            :style="{backgroundColor: color}"
            @click="changeBgColor(color)"
            )

</template>

<script>

import VueProductSpinner from './components/VueProductSpinner.vue'
import GitHubRibbon      from './components/GitHubRibbon.vue'

export default {
  name: 'app',

  data: function() {
    return {
      bgColor: '#CED2D8',
      colors: [
        '#CED2D8',
        '#303337',
        '#A46C00',
        '#A7B8CE',
        '#319289',
        '#3D4856'
      ],
      imgs: [
        '/imgs/1.png',
        '/imgs/2.png',
        '/imgs/3.png',
        '/imgs/4.png',
        '/imgs/5.png',
        '/imgs/6.png',
        '/imgs/7.png',
        '/imgs/8.png',
        '/imgs/9.png',
        '/imgs/10.png',
        '/imgs/11.png',
        '/imgs/12.png',
        '/imgs/13.png',
        '/imgs/14.png',
        '/imgs/15.png',
        '/imgs/16.png',
        '/imgs/17.png',
        '/imgs/18.png',
        '/imgs/19.png',
        '/imgs/20.png',
        '/imgs/21.png',
        '/imgs/22.png',
        '/imgs/23.png',
        '/imgs/24.png',
        '/imgs/25.png',
        '/imgs/26.png',
        '/imgs/27.png',
        '/imgs/28.png',
        '/imgs/29.png',
        '/imgs/30.png',
        '/imgs/31.png',
        '/imgs/32.png',
        '/imgs/33.png',
        '/imgs/34.png',
        '/imgs/35.png',
        '/imgs/36.png',
        '/imgs/37.png',
        '/imgs/38.png',
        '/imgs/39.png',
        '/imgs/40.png',
        '/imgs/41.png',
        '/imgs/42.png',
        '/imgs/43.png',
        '/imgs/44.png',
        '/imgs/45.png',
        '/imgs/46.png',
        '/imgs/47.png',
        '/imgs/48.png',
        '/imgs/49.png',
        '/imgs/50.png',
        '/imgs/51.png',
      ]
    }
  },

  methods: {
    changeBgColor(color) {
      this.bgColor = color
    }
  },

  components: {
    VueProductSpinner,
    GitHubRibbon
  }
}
</script>

<style lang="scss">
  body, #app {
    margin: 0;
    padding: 0;

    .vue-product-spinner {
      display: flex;
      justify-content: center;
      align-items: center;
      width: 100%;
      min-height: 100vh;
    }

    .color-selection {
      position: fixed;
      display: flex;
      justify-content: space-around;
      width: 100%;
      bottom: 2em;

      .color {
        flex-grow: 0;
        width: 50px;
        height: 50px;
        border-radius: 100%;
        border: white solid 5px;
        cursor: pointer;
      }
    }
  }
</style>