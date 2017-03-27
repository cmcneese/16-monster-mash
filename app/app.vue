<template lang="html">
<div class="app">
  <div class="app__sidebar">
    <h1>Build Monster </h1>

    <img :src="'/monsters/' + monsterParts.body[currentMonster.body] + '.png'" alt="">
    <img :src="'/monsters/' + monsterParts.mouth[currentMonster.mouth] + '.png'" alt="">
    <img :src="'/monsters/' + monsterParts.eyes[currentMonster.eyes] + '.png'" alt="">
  </div>
</div>
</template>

<script>
import Vue from 'vue';
import monsterParts from './monster-parts';

export default Vue.extend({
  data() {
    return {
      monsterParts,
      currentMonster: {
        body: 0,
        eyes: 0,
        mouth: 0,
        name: '',
      }
    }
  }
});
</script>
