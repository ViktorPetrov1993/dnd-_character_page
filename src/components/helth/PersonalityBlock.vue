<template>
  <section class="mainblock">
    <textarea name="" cols="30" rows="10" class="textm border_firstblock">
      PERSONALITY TRAITS
    </textarea>
    <textarea name="" cols="30" rows="10" class="textm border_secondblock">
      IDEALS
    </textarea>
    <textarea name="" cols="30" rows="10" class="textm border_thirdblock">
      BONDS
    </textarea>
    <textarea name="" cols="30" rows="10" class="textm border_fourthblock">
      FLAWS
    </textarea>
    <textarea name="" cols="30" rows="10" class="textm border_fivethblock">
      FEATURES & TRAITS
    </textarea>
  </section>
</template>

<script>
export default {
  name: "PersonalityBlock-comp",
  props: {
    msg: String,
  },
  data() {
    return {};
  },
  methods: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../assets/scss/main.scss";
.mainblock {
  @include flexColumn;
  @include flexstart;
  gap: 6px;
}

.border_firstblock,
.mediumtextarea {
  border-radius: 12px 12px 0 0;
  height: 125px;
}
.border_secondblock,
.border_thirdblock,
.mediumtextarea {
  height: 100px;
}
.border_fourthblock,
.mediumtextarea {
  border-radius: 0 0 12px 12px;
  height: 125px;
}
.border_fivethblock,
.mediumtextarea {
  height: 320px;
  border-radius: 12px;
}
textarea {
  color: black;
  background: radial-gradient(#fff0e8, #9b472e);
  border: 2px solid $border-color;
}
</style>
