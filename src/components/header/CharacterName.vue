<template>
  <section class="">
    <div class="header">
      <div class="header_rightpart">
        <div class="header_rightpart-textwithbtn" v-if="isCharacterName">
          <input type="text" v-model="charactername" class="input" />
          <button class="button button--info" @click="addCharacterField">
            add
          </button>
        </div>
        <div class="header_rightpart-textwithbtn" v-if="characterField">
          <div class="textxxl">{{ characterField }}</div>
          <button class="button button--info" @click="editCharacterField">
            edit
          </button>
        </div>
        <div class="textlx">CHARACTER NAME</div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "charactername-block",
  props: {},
  data() {
    return {
      charactername: null,
      characterField: null,
      editCharacter: false,
    };
  },
  computed: {
    isCharacterName() {
      return this.editCharacter || !this.characterField;
    },
  },
  methods: {
    addCharacterField() {
      this.characterField = this.charactername;
      this.editCharacter = false;
    },
    editCharacterField() {
      this.editCharacter = !this.editCharacter;
    },
  },
};
</script>

<style scoped lang="scss">
@import "../../assets/scss/main.scss";
.header {
  display: flex;
  flex-flow: row wrap;
  justify-content: space-between;
  align-items: center;
  padding: 4px;

  &_rightpart {
    @include flexColumn;
    justify-content: center;
    align-items: flex-start;
    gap: 4px;
    padding: 12px;
    border: 1px solid $border-color;
    border-radius: 12px;

    &-textwithbtn {
      @include flexrow;
      @include flexcenter;
      gap: 4px;
    }
  }
}
</style>
