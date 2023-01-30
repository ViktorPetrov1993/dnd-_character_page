<template>
  <div>
    <NameBlock>
      <template v-slot:CharacterName><CharacterName /> </template>
    </NameBlock>
    <StatsBlock>
      <template v-slot:MainStats><MainStats /> </template>
      <template v-slot:HelthBlock><HelthBlock /> </template>
      <template v-slot:PersonalityBlock><PersonalityBlock /> </template>
      <template v-slot:OtherProfeshions><OtherProfeshions /> </template>
      <template v-slot:CharacterImg><CharacterImg /> </template>
    </StatsBlock>
    <AdditionalNotes />
    <SpellList />
    <SpeshButton></SpeshButton>
    <AbilityList />
  </div>
</template>

<script>
// @ is an alias to /src
import NameBlock from "@/components/header/NameBlock.vue";
import StatsBlock from "@/components/stats/StatsBlock.vue";
import HelthBlock from "@/components/helth/HelthBlock.vue";
import PersonalityBlock from "@/components/helth/PersonalityBlock.vue";
import OtherProfeshions from "@/components/other/OtherProfeshions.vue";
import CharacterName from "@/components/header/CharacterName.vue";
import AdditionalNotes from "@/components/other/AdditionalNotes.vue";
import MainStats from "@/components/stats/MainStats.vue";
import CharacterImg from "@/components/CharacterImg.vue";
import SpellList from "@/components/spells/SpellList.vue";
import AbilityList from "@/components/abilitys/AbilityList.vue";
import SpeshButton from "@/components/SpeshButton.vue";

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
    AdditionalNotes,
    MainStats,
    SpeshButton,
    CharacterImg,
    SpellList,
    AbilityList,
  },
  data() {
    return {
      test: null,
      isActive: true,
    };
  },
  methods: {},
};
</script>

<style lang="scss">
img {
  max-width: 100% !important;
}
body {
  margin: 0;
  background: url(../assets/img/mainBG.jpg);
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  z-index: -1;
}
.textm,
.textl,
.textll,
.textlx,
.textxxl {
  color: #f9c1a1;
  border-radius: 12px;
  padding: 0 4px;
}
</style>
