<template>
  <div id="app">
      <Countdown date="October 28, 2019"></Countdown>
  </div>
</template>

<script>
import Countdown from './components/Countdown.vue';

export default {
    components: { Countdown },
}
</script>

<style>
#app{
    align-items: center;
    bottom: 0;
    display: flex;
    justify-content: center;
    left: 0;
    position: absolute;
    right: 0;
    top:0;
    background-color: #292b33;
    background-image: url("background.png");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
}
</style>
