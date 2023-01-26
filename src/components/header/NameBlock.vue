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
                <option value="Barbarian">Bard</option>
                <option value="Barbarian">Clirick</option>
                <option value="Barbarian">Druid</option>
                <option value="Barbarian">Warrior</option>
                <option value="Barbarian">Monk</option>
                <option value="Barbarian">Palladin</option>
                <option value="Barbarian">Ranger</option>
                <option value="Barbarian">Rogue</option>
                <option value="Barbarian">Sorcerer</option>
                <option value="Barbarian">Warlock</option>
                <option value="Barbarian">Wizzard</option>
              </select>
              <button class="button button--info">add</button>
            </div>
            <div class="textlx">CLASS</div>
          </div>
          <div class="firstrow_content">
            <div class="firstrow_content-textwithbtn">
              <select class="select" name="CLASS">
                <option value="Barbarian">Прислужник</option>
                <option value="Barbarian">Шарлатан</option>
                <option value="Barbarian">Преступник</option>
                <option value="Barbarian">Артист</option>
                <option value="Barbarian">Народный герой</option>
                <option value="Barbarian">Гильдейский ремесленник</option>
                <option value="Barbarian">Отшельник</option>
                <option value="Barbarian">Благородный</option>
                <option value="Barbarian">Чужеземец</option>
                <option value="Barbarian">Мудрец</option>
                <option value="Barbarian">Моряк</option>
                <option value="Barbarian">Солдат</option>
                <option value="Barbarian">Беспризорник</option>
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
                <option value="Barbarian">Dwarf</option>
                <option value="Barbarian">Elf</option>
                <option value="Barbarian">Halfling</option>
                <option value="Barbarian">Human</option>
                <option value="Barbarian">Dragonborn</option>
                <option value="Barbarian">Gnome</option>
                <option value="Barbarian">Half-elf</option>
                <option value="Barbarian">Half-orc</option>
                <option value="Barbarian">Tieflieng</option>
              </select>
              <button class="button button--info">add</button>
            </div>
            <div class="textlx">RACE</div>
          </div>
          <div class="firstrow_content">
            <div class="firstrow_content-textwithbtn">
              <select class="select" name="CLASS" id="">
                <option value="Barbarian">Законно добрые</option>
                <option value="Barbarian">Нейтрально добрые</option>
                <option value="Barbarian">Хаотично добрые</option>
                <option value="Barbarian">Законно нейтральные</option>
                <option value="Barbarian">Нейтральное</option>
                <option value="Barbarian">Хаотично нейтральные</option>
                <option value="Barbarian">Законно злые</option>
                <option value="Barbarian">Нейтрально злое</option>
                <option value="Barbarian">Хаотично злые</option>
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
