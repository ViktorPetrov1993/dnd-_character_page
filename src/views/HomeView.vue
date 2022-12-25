<template>
  <div class="CharacterPage lightversion">
    <HelloWorld />
    <StatsBlock>
      <template v-slot:test><HelthBlock /> </template>
    </StatsBlock>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import StatsBlock from "@/components/StatsBlock.vue";
import HelthBlock from "@/components/HelthBlock.vue";

export default {
  name: "HomeView",
  components: {
    HelloWorld,
    StatsBlock,
    HelthBlock,
  },
};
</script>

<style>
img {
  max-width: 100% !important;
}
body {
  margin: 0;
}
.lightversion {
  background: linear-gradient(to top, #eef3d2, #fc8884);
}
.darkversion {
  background: linear-gradient(to top, #af6480, #c3cee5);
}
</style>
