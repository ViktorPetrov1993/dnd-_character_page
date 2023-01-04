<template>
  <section class="stats">
    <div class="stats_main">
      <main-stats
        v-for="item in stats"
        :stat_name="item.name"
        v-model:stat_value="item.value"
        :key="item.name"
      />
    </div>
    <div class="stats_additional">
      <div class="firstblock">
        <input type="checkbox" class="firstblock_checkbox-bigbox" />
        <div class="textl fw-700">INSPIRATION</div>
      </div>
      <div class="secondblock">
        <input type="text" class="smallsquare" placeholder="+2" />
        <div class="textl fw-700">MASTER BONUS</div>
      </div>

      <div class="thirdblock">
        <label for="strength" class="thirdblock_content">
          <input type="radio" name="" id="strength" />
          <div class="thirdblock_content-value textm">+3</div>
          <div class="textm">Strength</div>
        </label>

        <label for="dexterity" class="thirdblock_content">
          <input type="radio" name="" id="dexterity" />
          <div class="thirdblock_content-value textm">+3</div>
          <div class="textm">Dexterity</div>
        </label>

        <label for="constitution" class="thirdblock_content">
          <input type="radio" name="" id="constitution" />
          <div class="thirdblock_content-value textm">+3</div>
          <div class="textm">Constitution</div>
        </label>

        <label for="intelligence" class="thirdblock_content">
          <input type="radio" name="" id="intelligence" />
          <div class="thirdblock_content-value textm">+3</div>
          <div class="textm">Intelligence</div>
        </label>

        <label for="wisdom" class="thirdblock_content">
          <input type="radio" name="" id="wisdom" />
          <div class="thirdblock_content-value textm">+3</div>
          <div class="textm">Wisdom</div>
        </label>

        <label for="charisma" class="thirdblock_content">
          <input type="radio" name="" id="charisma" />
          <div class="thirdblock_content-value textm">+3</div>
          <div class="textm">Charisma</div>
        </label>

        <div class="thirdblock_name textm">SAVING THROWS</div>
      </div>
      <div class="fourthblock">
        <label for="acrobatics" class="fourthblock_content">
          <input type="radio" name="" id="acrobatics" />
          <div class="fourthblock_content-value textm">+3</div>
          <div class="textm">Acrobatics(Dex)</div>
        </label>
        <label for="animal_Handling" class="fourthblock_content">
          <input type="radio" name="" id="animal_Handling" />
          <div class="fourthblock_content-value textm">+3</div>
          <div class="textm">Animal Handling(Wis)</div>
        </label>
        <label for="arcana" class="fourthblock_content">
          <input type="radio" name="" id="arcana" />
          <div class="fourthblock_content-value textm">+3</div>
          <div class="textm">Arcana(Int)</div>
        </label>
        <label for="athletics" class="fourthblock_content">
          <input type="radio" name="" id="athletics" />
          <div class="fourthblock_content-value textm">+3</div>
          <div class="textm">Athletics(Str)</div>
        </label>
        <label for="deception" class="fourthblock_content">
          <input type="radio" name="" id="deception" />
          <div class="fourthblock_content-value textm">+3</div>
          <div class="textm">Deception(Cha)</div>
        </label>
        <label for="history" class="fourthblock_content">
          <input type="radio" name="" id="history" />
          <div class="fourthblock_content-value textm">+3</div>
          <div class="textm">History(Int)</div>
        </label>
        <label for="insight" class="fourthblock_content">
          <input type="radio" name="" id="insight" />
          <div class="fourthblock_content-value textm">+3</div>
          <div class="textm">Insight(Wis)</div>
        </label>
        <label for="intimidation" class="fourthblock_content">
          <input type="radio" name="" id="intimidation" />
          <div class="fourthblock_content-value textm">+3</div>
          <div class="textm">Intimidation(Cha)</div>
        </label>
        <label for="investigation" class="fourthblock_content">
          <input type="radio" name="" id="investigation" />
          <div class="fourthblock_content-value textm">+3</div>
          <div class="textm">Investigation(Int)</div>
        </label>
        <label for="medicine" class="fourthblock_content">
          <input type="radio" name="" id="medicine" />
          <div class="fourthblock_content-value textm">+3</div>
          <div class="textm">Medicine(Wis)</div>
        </label>
        <label for="nature" class="fourthblock_content">
          <input type="radio" name="" id="nature" />
          <div class="fourthblock_content-value textm">+3</div>
          <div class="textm">Nature(Int)</div>
        </label>
        <label for="perception" class="fourthblock_content">
          <input type="radio" name="" id="perception" />
          <div class="fourthblock_content-value textm">+3</div>
          <div class="textm">Perception(Wis)</div>
        </label>
        <label for="performance" class="fourthblock_content">
          <input type="radio" name="" id="performance" />
          <div class="fourthblock_content-value textm">+3</div>
          <div class="textm">Performance(Cha)</div>
        </label>
        <label for="persuasion" class="fourthblock_content">
          <input type="radio" name="" id="persuasion" />
          <div class="fourthblock_content-value textm">+3</div>
          <div class="textm">Persuasion(Cha)</div>
        </label>
        <label for="religion" class="fourthblock_content">
          <input type="radio" name="" id="religion" />
          <div class="fourthblock_content-value textm">+3</div>
          <div class="textm">Religion(Int)</div>
        </label>
        <label for="sleight_of_Hand" class="fourthblock_content">
          <input type="radio" name="" id="sleight_of_Hand" />
          <div class="fourthblock_content-value textm">+3</div>
          <div class="textm">Sleight of Hand(Dex)</div>
        </label>
        <label for="stealth" class="fourthblock_content">
          <input type="radio" name="" id="stealth" />
          <div class="fourthblock_content-value textm">+3</div>
          <div class="textm">Stealth(Dex)</div>
        </label>
        <label for="survival" class="fourthblock_content">
          <input type="radio" name="" id="survival" />
          <div class="fourthblock_content-value textm">+3</div>
          <div class="textm">Survival(Wis)</div>
        </label>
        <div class="thirdblock_name textl">SKILLS</div>
      </div>
    </div>
    <slot name="HelthBlock"> </slot>
    <slot name="PersonalityBlock"> </slot>
    <slot name="OtherProfeshions"> </slot>
  </section>
</template>

<script>
import MainStats from "./MainStats.vue";
export default {
  name: "StatsBlock-comp",
  components: { MainStats },
  props: {
    msg: String,
  },
  data() {
    return {
      stats: [
        {
          name: "STRENGTH",
          value: 10,
        },
        {
          name: "DEXTERITY",
          value: 10,
        },
        {
          name: "CONSTITUTION",
          value: 10,
        },
        {
          name: "INTELLIGENCE",
          value: 10,
        },
        {
          name: "WISDOM",
          value: 10,
        },
        {
          name: "CHARISMA",
          value: 10,
        },
      ],
    };
  },
  computed: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../assets/scss/main.scss";
.stats {
  display: flex;
  flex-flow: row wrap;
  @include flexstart;
  gap: 12px;
  padding-top: 8px;

  &_main {
    @include flexColumn;
    @include flexcenter;
    gap: 28px;
  }
  &_additional {
    @include flexColumn;
    @include flexstart;
    gap: 16px;
  }
}
.firstblock,
.secondblock {
  display: flex;
  flex-flow: row nowrap;
  justify-content: space-between;
  align-items: center;
  border: 1px solid $border-color;
  border-radius: 12px;
  padding: 10px 8px;
  width: 93%;
}
.thirdblock,
.fourthblock {
  @include flexColumn;
  @include flexstart;
  gap: 8px;
  border: 1px solid $border-color;
  border-radius: 12px;
  padding: 12px 8px;
  width: 93%;

  &_content {
    display: flex;
    gap: 4px;

    &_value {
      max-width: 20px;
      border-bottom: 1px solid $border-color;
    }
  }

  &_name {
    margin-left: 25px;
  }
}
</style>
