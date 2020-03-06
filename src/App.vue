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
#app{
    align-items: center;
    bottom: 0;
    background-color: #292b33;
    display: flex;
    justify-content: center;
    left: 0;
    position: absolute;
    right: 0;
    top:0;
}
</style>
