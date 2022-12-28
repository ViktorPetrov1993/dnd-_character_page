<template>
  <section class="stats">
    <div>
      <div>
        <div class="stats_main">
          <div class="textl fw-700">STRENGTH</div>
          <input type="number" v-model="strength" class="squareinput textxxl" />
        </div>
        <div class="stats_main_value" v-if="isCharacterName">
          {{ strBonus.bonus }}
        </div>
      </div>
      <div>
        <div class="stats_main">
          <div class="textl fw-700">DEXTERITY</div>
          <input type="number" class="squareinput textxxl" />
        </div>
        <div class="stats_main_value">+3</div>
      </div>
      <div>
        <div class="stats_main">
          <div class="textl fw-700">CONSTITUTION</div>
          <input type="number" class="squareinput textxxl" />
        </div>
        <div class="stats_main_value">+3</div>
      </div>
      <div>
        <div class="stats_main">
          <div class="textl fw-700">INTELLIGENCE</div>
          <input type="number" class="squareinput textxxl" />
        </div>
        <div class="stats_main_value">+3</div>
      </div>
      <div>
        <div class="stats_main">
          <div class="textl fw-700">WISDOM</div>
          <input type="number" class="squareinput textxxl" />
        </div>
        <div class="stats_main_value">+3</div>
      </div>
      <div>
        <div class="stats_main">
          <div class="textl fw-700">CHARISMA</div>
          <input type="number" class="squareinput textxxl" />
        </div>
        <div class="stats_main_value">+3</div>
      </div>
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
          <div class="thirdblock_content-value menutextm">+3</div>
          <div class="menutextm">Strength</div>
        </label>
        <label for="dexterity" class="thirdblock_content">
          <input type="radio" name="" id="dexterity" />
          <div class="thirdblock_content-value menutextm">+3</div>
          <div class="menutextm">Dexterity</div>
        </label>
        <label for="constitution" class="thirdblock_content">
          <input type="radio" name="" id="constitution" />
          <div class="thirdblock_content-value menutextm">+3</div>
          <div class="menutextm">Constitution</div>
        </label>
        <label for="intelligence" class="thirdblock_content">
          <input type="radio" name="" id="intelligence" />
          <div class="thirdblock_content-value menutextm">+3</div>
          <div class="menutextm">Intelligence</div>
        </label>
        <label for="wisdom" class="thirdblock_content">
          <input type="radio" name="" id="wisdom" />
          <div class="thirdblock_content-value menutextm">+3</div>
          <div class="menutextm">Wisdom</div>
        </label>
        <label for="charisma" class="thirdblock_content">
          <input type="radio" name="" id="charisma" />
          <div class="thirdblock_content-value menutextm">+3</div>
          <div class="menutextm">Charisma</div>
        </label>
        <div class="thirdblock_name menutextm">SAVING THROWS</div>
      </div>
      <div class="fourthblock">
        <label for="acrobatics" class="fourthblock_content">
          <input type="radio" name="" id="acrobatics" />
          <div class="fourthblock_content-value menutextm">+3</div>
          <div class="menutextm">Acrobatics(Dex)</div>
        </label>
        <label for="animal_Handling" class="fourthblock_content">
          <input type="radio" name="" id="animal_Handling" />
          <div class="fourthblock_content-value menutextm">+3</div>
          <div class="menutextm">Animal Handling(Wis)</div>
        </label>
        <label for="arcana" class="fourthblock_content">
          <input type="radio" name="" id="arcana" />
          <div class="fourthblock_content-value menutextm">+3</div>
          <div class="menutextm">Arcana(Int)</div>
        </label>
        <label for="athletics" class="fourthblock_content">
          <input type="radio" name="" id="athletics" />
          <div class="fourthblock_content-value menutextm">+3</div>
          <div class="menutextm">Athletics(Str)</div>
        </label>
        <label for="deception" class="fourthblock_content">
          <input type="radio" name="" id="deception" />
          <div class="fourthblock_content-value menutextm">+3</div>
          <div class="menutextm">Deception(Cha)</div>
        </label>
        <label for="history" class="fourthblock_content">
          <input type="radio" name="" id="history" />
          <div class="fourthblock_content-value menutextm">+3</div>
          <div class="menutextm">History(Int)</div>
        </label>
        <label for="insight" class="fourthblock_content">
          <input type="radio" name="" id="insight" />
          <div class="fourthblock_content-value menutextm">+3</div>
          <div class="menutextm">Insight(Wis)</div>
        </label>
        <label for="intimidation" class="fourthblock_content">
          <input type="radio" name="" id="intimidation" />
          <div class="fourthblock_content-value menutextm">+3</div>
          <div class="menutextm">Intimidation(Cha)</div>
        </label>
        <label for="investigation" class="fourthblock_content">
          <input type="radio" name="" id="investigation" />
          <div class="fourthblock_content-value menutextm">+3</div>
          <div class="menutextm">Investigation(Int)</div>
        </label>
        <label for="medicine" class="fourthblock_content">
          <input type="radio" name="" id="medicine" />
          <div class="fourthblock_content-value menutextm">+3</div>
          <div class="menutextm">Medicine(Wis)</div>
        </label>
        <label for="nature" class="fourthblock_content">
          <input type="radio" name="" id="nature" />
          <div class="fourthblock_content-value menutextm">+3</div>
          <div class="menutextm">Nature(Int)</div>
        </label>
        <label for="perception" class="fourthblock_content">
          <input type="radio" name="" id="perception" />
          <div class="fourthblock_content-value menutextm">+3</div>
          <div class="menutextm">Perception(Wis)</div>
        </label>
        <label for="performance" class="fourthblock_content">
          <input type="radio" name="" id="performance" />
          <div class="fourthblock_content-value menutextm">+3</div>
          <div class="menutextm">Performance(Cha)</div>
        </label>
        <label for="persuasion" class="fourthblock_content">
          <input type="radio" name="" id="persuasion" />
          <div class="fourthblock_content-value menutextm">+3</div>
          <div class="menutextm">Persuasion(Cha)</div>
        </label>
        <label for="religion" class="fourthblock_content">
          <input type="radio" name="" id="religion" />
          <div class="fourthblock_content-value menutextm">+3</div>
          <div class="menutextm">Religion(Int)</div>
        </label>
        <label for="sleight_of_Hand" class="fourthblock_content">
          <input type="radio" name="" id="sleight_of_Hand" />
          <div class="fourthblock_content-value menutextm">+3</div>
          <div class="menutextm">Sleight of Hand(Dex)</div>
        </label>
        <label for="stealth" class="fourthblock_content">
          <input type="radio" name="" id="stealth" />
          <div class="fourthblock_content-value menutextm">+3</div>
          <div class="menutextm">Stealth(Dex)</div>
        </label>
        <label for="survival" class="fourthblock_content">
          <input type="radio" name="" id="survival" />
          <div class="fourthblock_content-value menutextm">+3</div>
          <div class="menutextm">Survival(Wis)</div>
        </label>
        <div class="thirdblock_name">SKILLS</div>
      </div>
    </div>
    <slot name="HelthBlock"> </slot>
    <slot name="PersonalityBlock"> </slot>
    <slot name="OtherProfeshions"> </slot>
  </section>
</template>

<script>
export default {
  name: "StatsBlock-comp",
  components: {},
  props: {
    msg: String,
  },
  data() {
    return {
      strength: null,
      strBonus: [
        { str: 1, bonus: -5 },
        { str: 3, bonus: -4 },
      ],
    };
  },
  computed: {
    isCharacterName() {
      return this.strength == this.strBonus.[str];
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/main.scss";
.stats {
  display: flex;
  flex-flow: row wrap;
  @include flexstart;
  gap: 12px;
  padding-top: 8px;

  &_main {
    @include flexColumn;
    @include flexcenter;
    padding-top: 8px;

    &_value {
      border: 1px solid black;
      border-radius: 12px;
      margin-left: 45px;
      width: 30px;
    }
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
  border: 1px solid black;
  border-radius: 12px;
  padding: 10px 8px;
  width: 93%;
}
.thirdblock,
.fourthblock {
  @include flexColumn;
  @include flexstart;
  gap: 8px;
  border: 1px solid black;
  border-radius: 12px;
  padding: 12px 8px;
  width: 93%;

  &_content {
    display: flex;
    gap: 4px;

    &_value {
      max-width: 20px;
      border-bottom: 1px solid black;
    }
  }

  &_name {
    margin-left: 25px;
  }
}
</style>
