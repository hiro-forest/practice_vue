<template>
  <div>
    <div v-if="test === false" v-on:click="aoao()" class="hoge">{{ msg }}</div>
    <div v-if="test === true" v-on:click="aoao()" class="piyo">
      {{ henkou }}
    </div>
  </div>
</template>

<style>
.hoge {
  width: 500px;
  height: 500px;
  background-color: aqua;
}
.piyo {
  width: 500px;
  height: 500px;
  background-color: rgb(185, 17, 59);
}
</style>

<script>
export default {
  data() {
    return {
      msg: 'アイウエオ',
      henkou: 'かきくけこ',
      test: true
    }
  },
  methods: {
    aoao() {
      if (this.test === false) {
        this.test = true
      } else {
        this.test = false
      }
    }
  }
}
</script>
