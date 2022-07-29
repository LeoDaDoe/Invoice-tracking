<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import HelloWorld from "@/components/HelloWorld.vue"; // @ is an alias to /src
import WorkHourGraph from "../components/WorkHoursComponents/WorkHourGraph.vue";

@Component({
  components: {
    HelloWorld,
    WorkHourGraph,
  },
})
export default class HomeView extends Vue {}
</script>
