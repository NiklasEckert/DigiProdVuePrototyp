<template>
  <RootComp />
</template>

<script>
import RootComp from "@/components/RootComp";
import {provide} from "vue";

export default {
  name: 'App',
  components: {
    RootComp
  },
  mounted() {
    this.comps = []
    for(let i=1;i<=500;i++) {
      this.comps.push({
        id: i,
        articleNumber:  Math.random().toString(36).substring(2,7),
        orderNumber: Math.random().toString(36).substring(2,7),
        birthdate: "09.01.2022",
        location: "Bingen"});
      console.log(i);
    }

    provide('comps', this.comps)
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
