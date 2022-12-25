<template>
  <section class="stats">
    <div>
      <div>
        <div class="stats_main">
          <div class="stats_main_textl">STRENGTH</div>
          <input type="text" class="stats_main_input" />
        </div>
        <div class="stats_main_value">+3</div>
        <button class="add">add</button>
      </div>
      <div>
        <div class="stats_main">
          <div class="stats_main_textl">DEXTERITY</div>
          <input type="text" class="stats_main_input" />
        </div>
        <div class="stats_main_value">+3</div>
        <button class="add">add</button>
      </div>
      <div>
        <div class="stats_main">
          <div class="stats_main_textl">CONSTITUTION</div>
          <input type="text" class="stats_main_input" />
        </div>
        <div class="stats_main_value">+3</div>
        <button class="add">add</button>
      </div>
      <div>
        <div class="stats_main">
          <div class="stats_main_textl">INTELLIGENCE</div>
          <input type="text" class="stats_main_input" />
        </div>
        <div class="stats_main_value">+3</div>
        <button class="add">add</button>
      </div>
      <div>
        <div class="stats_main">
          <div class="stats_main_textl">WISDOM</div>
          <input type="text" class="stats_main_input" />
        </div>
        <div class="stats_main_value">+3</div>
        <button class="add">add</button>
      </div>
      <div>
        <div class="stats_main">
          <div class="stats_main_textl">CHARISMA</div>
          <input type="text" class="stats_main_input" />
        </div>
        <div class="stats_main_value">+3</div>
        <button class="add">add</button>
      </div>
    </div>
    <div class="stats_additional">
      <div class="stats_additional_firstblock">
        <input
          type="checkbox"
          class="stats_additional_firstblock_inspiration"
        />
        <div class="stats_additional_firstblock_textl">INSPIRATION</div>
      </div>
      <div class="stats_additional_secondblock">
        <input type="text" class="stats_additional_secondblock_masterbonus" />
        <div class="stats_additional_secondblock_textl">MASTER BONUS</div>
      </div>
      <div class="stats_additional_thirdblock">
        <label for="strength" class="stats_additional_thirdblock_bonus">
          <input type="radio" name="" id="strength" />
          <div class="stats_additional_thirdblock_bonus_value menutextm">
            +3
          </div>
          <div class="menutextm">Strength</div>
        </label>
        <label for="dexterity" class="stats_additional_thirdblock_bonus">
          <input type="radio" name="" id="dexterity" />
          <div class="stats_additional_thirdblock_bonus_value menutextm">
            +3
          </div>
          <div class="menutextm">Dexterity</div>
        </label>
        <label for="constitution" class="stats_additional_thirdblock_bonus">
          <input type="radio" name="" id="constitution" />
          <div class="stats_additional_thirdblock_bonus_value menutextm">
            +3
          </div>
          <div class="menutextm">Constitution</div>
        </label>
        <label for="intelligence" class="stats_additional_thirdblock_bonus">
          <input type="radio" name="" id="intelligence" />
          <div class="stats_additional_thirdblock_bonus_value menutextm">
            +3
          </div>
          <div class="menutextm">Intelligence</div>
        </label>
        <label for="wisdom" class="stats_additional_thirdblock_bonus">
          <input type="radio" name="" id="wisdom" />
          <div class="stats_additional_thirdblock_bonus_value menutextm">
            +3
          </div>
          <div class="menutextm">Wisdom</div>
        </label>
        <label for="charisma" class="stats_additional_thirdblock_bonus">
          <input type="radio" name="" id="charisma" />
          <div class="stats_additional_thirdblock_bonus_value menutextm">
            +3
          </div>
          <div class="menutextm">Charisma</div>
        </label>
        <div class="stats_additional_thirdblock_name menutextm">
          SAVING THROWS
        </div>
      </div>
      <div class="stats_additional_fourthblock">
        <label for="acrobatics" class="stats_additional_fourthblock_bonus">
          <input type="radio" name="" id="acrobatics" />
          <div class="stats_additional_fourthblock_bonus_value menutextm">
            +3
          </div>
          <div class="menutextm">Acrobatics(Dex)</div>
        </label>
        <label for="animal_Handling" class="stats_additional_fourthblock_bonus">
          <input type="radio" name="" id="animal_Handling" />
          <div class="stats_additional_fourthblock_bonus_value menutextm">
            +3
          </div>
          <div class="menutextm">Animal Handling(Wis)</div>
        </label>
        <label for="arcana" class="stats_additional_fourthblock_bonus">
          <input type="radio" name="" id="arcana" />
          <div class="stats_additional_fourthblock_bonus_value menutextm">
            +3
          </div>
          <div class="menutextm">Arcana(Int)</div>
        </label>
        <label for="athletics" class="stats_additional_fourthblock_bonus">
          <input type="radio" name="" id="athletics" />
          <div class="stats_additional_fourthblock_bonus_value menutextm">
            +3
          </div>
          <div class="menutextm">Athletics(Str)</div>
        </label>
        <label for="deception" class="stats_additional_fourthblock_bonus">
          <input type="radio" name="" id="deception" />
          <div class="stats_additional_fourthblock_bonus_value menutextm">
            +3
          </div>
          <div class="menutextm">Deception(Cha)</div>
        </label>
        <label for="history" class="stats_additional_fourthblock_bonus">
          <input type="radio" name="" id="history" />
          <div class="stats_additional_fourthblock_bonus_value menutextm">
            +3
          </div>
          <div class="menutextm">History(Int)</div>
        </label>
        <label for="insight" class="stats_additional_fourthblock_bonus">
          <input type="radio" name="" id="insight" />
          <div class="stats_additional_fourthblock_bonus_value menutextm">
            +3
          </div>
          <div class="menutextm">Insight(Wis)</div>
        </label>
        <label for="intimidation" class="stats_additional_fourthblock_bonus">
          <input type="radio" name="" id="intimidation" />
          <div class="stats_additional_fourthblock_bonus_value menutextm">
            +3
          </div>
          <div class="menutextm">Intimidation(Cha)</div>
        </label>
        <label for="investigation" class="stats_additional_fourthblock_bonus">
          <input type="radio" name="" id="investigation" />
          <div class="stats_additional_fourthblock_bonus_value menutextm">
            +3
          </div>
          <div class="menutextm">Investigation(Int)</div>
        </label>
        <label for="medicine" class="stats_additional_fourthblock_bonus">
          <input type="radio" name="" id="medicine" />
          <div class="stats_additional_fourthblock_bonus_value menutextm">
            +3
          </div>
          <div class="menutextm">Medicine(Wis)</div>
        </label>
        <label for="nature" class="stats_additional_fourthblock_bonus">
          <input type="radio" name="" id="nature" />
          <div class="stats_additional_fourthblock_bonus_value menutextm">
            +3
          </div>
          <div class="menutextm">Nature(Int)</div>
        </label>
        <label for="perception" class="stats_additional_fourthblock_bonus">
          <input type="radio" name="" id="perception" />
          <div class="stats_additional_fourthblock_bonus_value menutextm">
            +3
          </div>
          <div class="menutextm">Perception(Wis)</div>
        </label>
        <label for="performance" class="stats_additional_fourthblock_bonus">
          <input type="radio" name="" id="performance" />
          <div class="stats_additional_fourthblock_bonus_value menutextm">
            +3
          </div>
          <div class="menutextm">Performance(Cha)</div>
        </label>
        <label for="persuasion" class="stats_additional_fourthblock_bonus">
          <input type="radio" name="" id="persuasion" />
          <div class="stats_additional_fourthblock_bonus_value menutextm">
            +3
          </div>
          <div class="menutextm">Persuasion(Cha)</div>
        </label>
        <label for="religion" class="stats_additional_fourthblock_bonus">
          <input type="radio" name="" id="religion" />
          <div class="stats_additional_fourthblock_bonus_value menutextm">
            +3
          </div>
          <div class="menutextm">Religion(Int)</div>
        </label>
        <label for="sleight_of_Hand" class="stats_additional_fourthblock_bonus">
          <input type="radio" name="" id="sleight_of_Hand" />
          <div class="stats_additional_fourthblock_bonus_value menutextm">
            +3
          </div>
          <div class="menutextm">Sleight of Hand(Dex)</div>
        </label>
        <label for="stealth" class="stats_additional_fourthblock_bonus">
          <input type="radio" name="" id="stealth" />
          <div class="stats_additional_fourthblock_bonus_value menutextm">
            +3
          </div>
          <div class="menutextm">Stealth(Dex)</div>
        </label>
        <label for="survival" class="stats_additional_fourthblock_bonus">
          <input type="radio" name="" id="survival" />
          <div class="stats_additional_fourthblock_bonus_value menutextm">
            +3
          </div>
          <div class="menutextm">Survival(Wis)</div>
        </label>
        <div class="stats_additional_thirdblock_name">SKILLS</div>
      </div>
    </div>
    <slot name="test"> </slot>
    <PersonalityBlock />
  </section>
</template>

<script>
import PersonalityBlock from "@/components/PersonalityBlock.vue";

export default {
  name: "StatsBlock-comp",
  components: {
    PersonalityBlock,
  },
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/main.scss";

.stats {
  display: flex;
  flex-flow: row wrap;
  justify-content: flex-start;
  align-items: flex-start;
  gap: 12px;
  padding-top: 16px;

  &_main {
    display: flex;
    flex-flow: column;
    justify-content: center;
    align-items: center;

    &_textl {
      padding-bottom: 4px;
    }

    &_input {
      width: 60px;
      min-height: 70px;
      text-align: center;
      border-radius: 12px;
    }

    &_value {
      border: 1px solid black;
      border-radius: 12px;
      margin-left: 45px;
      width: 30px;
    }
  }
  &_additional {
    display: flex;
    flex-flow: column;
    justify-content: flex-start;
    align-items: flex-start;
    gap: 16px;

    &_firstblock,
    &_secondblock {
      display: flex;
      flex-flow: row nowrap;
      justify-content: space-between;
      align-items: center;
      border: 1px solid black;
      border-radius: 12px;
      padding: 10px 8px;
      width: 93%;

      &_inspiration {
        width: 20px;
        height: 20px;
      }

      &_masterbonus {
        width: 20px;
        height: 20px;
        text-align: center;
      }
    }

    &_thirdblock,
    &_fourthblock {
      display: flex;
      flex-flow: column;
      justify-content: flex-start;
      align-items: flex-start;
      gap: 8px;
      border: 1px solid black;
      border-radius: 12px;
      padding: 12px 8px;
      width: 93%;

      &_bonus {
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
  }
}
</style>
