<template>
  <section class="">
    <div class="header">
      <slot name="CharacterName"> </slot>
      <div class="header_leftpart">
        <div class="firstrow">
          <div class="firstrow_content">
            <div class="firstrow_content-textwithbtn">
              <select class="select" name="CLASS" id="">
                <option value="Barbarian">Barbarian</option>
                <option value="Barbarian">Barbarian</option>
                <option value="Barbarian">Barbarian</option>
                <option value="Barbarian">Barbarian</option>
              </select>
              <button class="button button--info">add</button>
            </div>
            <div class="textlx">CLASS</div>
          </div>
          <div class="firstrow_content">
            <div class="firstrow_content-textwithbtn">
              <select class="select" name="CLASS">
                <option value="Barbarian">Barbarian</option>
                <option value="Barbarian">Barbarian</option>
                <option value="Barbarian">Barbarian</option>
                <option value="Barbarian">Barbarian</option>
              </select>
              <button class="button button--info">add</button>
            </div>
            <div class="textlx">BACKGROUND</div>
          </div>
          <div class="firstrow_content">
            <div class="firstrow_content-textwithbtn" v-if="isPlayerName">
              <input type="text" v-model="playername" class="smallinput" />
              <button class="button button--info" @click="addPlayername">
                add
              </button>
            </div>
            <div class="header_rightpart-textwithbtn" v-if="playerField">
              <div class="textl">{{ playerField }}</div>
              <button class="button button--info" @click="editPlayername">
                edit
              </button>
            </div>
            <div class="textlx">PLAYER NAME</div>
          </div>
        </div>
        <div class="secondrow">
          <div class="firstrow_content">
            <div class="firstrow_content-textwithbtn">
              <select class="select" name="CLASS" id="">
                <option value="Barbarian">Barbarian</option>
                <option value="Barbarian">Barbarian</option>
                <option value="Barbarian">Barbarian</option>
                <option value="Barbarian">Barbarian</option>
              </select>
              <button class="button button--info">add</button>
            </div>
            <div class="textlx">RACE</div>
          </div>
          <div class="firstrow_content">
            <div class="firstrow_content-textwithbtn">
              <select class="select" name="CLASS" id="">
                <option value="Barbarian">Barbarian</option>
                <option value="Barbarian">Barbarian</option>
                <option value="Barbarian">Barbarian</option>
                <option value="Barbarian">Barbarian</option>
              </select>
              <button class="button button--info">add</button>
            </div>
            <div class="textlx">ALIGNMENT</div>
          </div>
          <div class="firstrow_content">
            <div class="firstrow_content-textwithbtn" v-if="isExpPoints">
              <input type="text" v-model="exppoints" class="smallinput" />
              <button class="button button--info" @click="addExpPoints">
                add
              </button>
            </div>
            <div class="header_rightpart-textwithbtn" v-if="expField">
              <div class="textl">{{ expField }}</div>
              <button class="button button--info" @click="editExpPoints">
                edit
              </button>
            </div>
            <div class="textlx">EXPERIENCE POINTS</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "name-block",
  props: {},
  data() {
    return {
      playername: null,
      playerField: null,
      editPlayer: false,
      exppoints: null,
      expField: null,
      editExp: false,
    };
  },
  computed: {
    isPlayerName() {
      return this.editPlayer || !this.playerField;
    },
    isExpPoints() {
      return this.editExp || !this.expField;
    },
  },
  methods: {
    addPlayername() {
      this.playerField = this.playername;
      this.editPlayer = false;
    },
    editPlayername() {
      this.editPlayer = !this.editPlayer;
    },
    addExpPoints() {
      this.expField = this.exppoints;
      this.editExp = false;
    },
    editExpPoints() {
      this.editExp = !this.editExp;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
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

  &_leftpart {
    @include flexColumn;
    @include flexcenter;
    border: 1px solid $border-color;
    padding: 12px;
    border-radius: 12px;
  }
  .firstrow,
  .secondrow {
    display: flex;
    flex-flow: row wrap;
    @include flexcenter;
    gap: 4px;

    &_content {
      @include flexColumn;
      justify-content: center;
      align-items: flex-start;
      gap: 4px;

      &-textwithbtn {
        @include flexrow;
        gap: 4px;
      }
    }
  }
  .textlx {
    border-top: 1px solid $border-color;
    width: 98%;
    text-align: start;
    padding: 4px;
  }
}
</style>
