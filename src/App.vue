<template>
  <div id="app">
    <Countdown eventdate="March 31, 2020" startdate="October 28, 2019"></Countdown>
  </div>
</template>

<script>
import Countdown from "./components/Countdown.vue";

export default {
  components: { Countdown }
};
</script>

<style>
#app {
  align-items: center;
  bottom: 0;
  display: flex;
  justify-content: center;
  left: 0;
  position: absolute;
  right: 0;
  top: 0;
  background-color: #000000;
  background-image: url("background.png");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
}
</style>
