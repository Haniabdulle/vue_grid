<template>
<!-- app div is a parent div -->
  <div id="app">
    <div id="box">
      <twitter-data></twitter-data>
    </div>
  </div>
</template>

<script>
// twitter data component will get imported from src/components/twitterdata
import TwitterData from "@/components/TwitterData.vue";
export default {
  name: "App",
  components: {
    TwitterData,
  },
};
</script>

<style scoped>
#box{
  display: grid;
  grid-auto-flow: row;
}
</style>
