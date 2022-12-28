<template>
  <div :class="['CharacterPage', 'lightversion', { darkversion: isActive }]">
    <NameBlock>
      <template v-slot:CharacterName><CharacterName /> </template>
    </NameBlock>
    <StatsBlock>
      <template v-slot:HelthBlock><HelthBlock /> </template>
      <template v-slot:PersonalityBlock><PersonalityBlock /> </template>
      <template v-slot:OtherProfeshions><OtherProfeshions /> </template>
    </StatsBlock>
    <button
      :class="[
        'button',
        { 'button--primary': isActive },
        { 'button--secondary': !isActive },
      ]"
      @click="isActive = !isActive"
    >
      dark
    </button>
    <!-- <SpeshButton @testEvent="test_met"
    {{ test }}></SpeshButton> -->
  </div>
</template>

<script>
// @ is an alias to /src
import NameBlock from "@/components/NameBlock.vue";
import StatsBlock from "@/components/StatsBlock.vue";
import HelthBlock from "@/components/HelthBlock.vue";
import PersonalityBlock from "@/components/PersonalityBlock.vue";
import OtherProfeshions from "@/components/OtherProfeshions.vue";
import CharacterName from "@/components/CharacterName.vue";

// import SpeshButton from "@/components/SpeshButton.vue";

export default {
  name: "HomeView",
  props: {},
  components: {
    NameBlock,
    StatsBlock,
    HelthBlock,
    PersonalityBlock,
    OtherProfeshions,
    CharacterName,
    // SpeshButton,
  },
  data() {
    return {
      test: null,
      isActive: true,
    };
  },
  methods: {
    // test_met(value) {
    //   this.test = value;
    // },
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
