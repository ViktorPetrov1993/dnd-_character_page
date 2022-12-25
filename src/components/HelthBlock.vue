<template>
  <section class="helthblock">
    <div class="helthblock_firstblock">
      <div class="helthblock_firstblock_armor">
        <div class="helthblock_firstblock_armor_leftblock">
          <div class="helthblock_firstblock_armor_leftblock_value">16</div>
          <div class="stats_main_textl">
            ARMOR <br />
            CLASS
          </div>
        </div>
        <div class="helthblock_firstblock_armor_middleblock">
          <input
            type="text"
            class="helthblock_firstblock_armor_middleblock_value"
          />
          <div class="stats_main_textl">INITIATIVE</div>
          <button class="add">add</button>
        </div>
        <div class="helthblock_firstblock_armor_rightblock">
          <input
            type="text"
            class="helthblock_firstblock_armor_rightblock_value"
          />
          <div class="stats_main_textl">SPEED</div>
          <button class="add">add</button>
        </div>
      </div>
      <div class="helthblock_firstblock_helth">
        <div class="helthblock_firstblock_helth_maxhelth">
          <div class="textll">Hit Point Max</div>
          <input
            type="text"
            class="helthblock_firstblock_helth_maxhelth_value"
          />
          <button class="add">add</button>
        </div>
        <input type="text" class="helthblock_firstblock_helth_currenthelth" />
        <div class="helthblock_firstblock_helth_named menutextm">
          CURRENT HIT POINTS
        </div>
      </div>
      <div class="helthblock_firstblock_temporhelth">
        <input type="text" class="helthblock_firstblock_temporhelth_value" />
        <div class="menutextm">TEMPORARY HIT POINTS</div>
      </div>
      <div class="helthblock_firstblock_bottomblocks">
        <div class="helthblock_firstblock_bottomblocks_helthdice">
          <div class="helthblock_firstblock_bottomblocks_helthdice_total">
            <div class="textll">Total</div>
            <input
              type="text"
              class="helthblock_firstblock_bottomblocks_helthdice_total_value"
            />
          </div>
          <input
            type="text"
            class="helthblock_firstblock_bottomblocks_helthdice_value"
          />
          <div class="menutextl">HIT DICE</div>
        </div>
        <div class="helthblock_firstblock_bottomblocks_deathdice">
          <div class="helthblock_firstblock_bottomblocks_deathdice_check">
            <label
              for="succes"
              class="helthblock_firstblock_bottomblocks_deathdice_check_succes"
              ><div class="menutextl">SUCCESSES</div>
              <input
                type="radio"
                id="succes"
                v-for="n of 3"
                :key="'succes' + n"
              />{{ n }}
            </label>
            <label
              for="fail"
              class="helthblock_firstblock_bottomblocks_deathdice_check_fail"
              ><div class="menutextl">FAILURES</div>
              <input
                type="radio"
                id="fail"
                v-for="n of 3"
                :key="'fail' + n"
              />{{ n }}
            </label>
          </div>
          <div class="menutextl">DEATH SAVES</div>
        </div>
      </div>
    </div>
    <div class="helthblock_secondblock">
      <div class="helthblock_secondblock_armor">
        <div>
          <div class="helthblock_secondblock_armor_text menutextm">ARMOR</div>
          <input
            type="text"
            v-model="text"
            class="helthblock_secondblock_armor_value"
          />
          <button class="add" @click="addArmor">add</button>
        </div>
        <ul class="">
          <li v-for="n of armor" :key="'item' + n" @click="remove(n)">
            {{ n }}
          </li>
        </ul>
      </div>
      <div class="helthblock_secondblock_weapon">
        <div class="helthblock_secondblock_weapon_items">
          <div class="helthblock_secondblock_weapon_items_type">
            <div
              class="helthblock_secondblock_weapon_items_type_text menutextm"
            >
              NAME
            </div>
            <input
              type="text"
              v-model="weaponname"
              class="helthblock_secondblock_weapon_items_type_firstvalue"
            />
          </div>
          <div class="helthblock_secondblock_weapon_items_type">
            <div
              class="helthblock_secondblock_weapon_items_type_text menutextm"
            >
              ATK BONUS
            </div>
            <input
              type="text"
              v-model="weaponname"
              class="helthblock_secondblock_weapon_items_type_secondvalue"
            />
          </div>
          <div class="helthblock_secondblock_weapon_items_type">
            <div
              class="helthblock_secondblock_weapon_items_type_text menutextm"
            >
              DAMAGE/TYPE
            </div>
            <input
              type="text"
              v-model="weaponname"
              class="helthblock_secondblock_weapon_items_type_thirdvalue"
            />
          </div>
          <button class="add" @click="addWeapon">add</button>
        </div>
        <ul class="">
          <li
            v-for="n of weapon"
            :key="'weaponitem' + n"
            @click="removeWeapon(n)"
          >
            {{ n }}
          </li>
        </ul>
      </div>
      <div class="helthblock_secondblock_blockname menutextm">
        ATTACKS & SPELLCASTING
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "HelthBlock-comp",
  props: {
    msg: String,
  },
  data() {
    return {
      text: null,
      armor: [],
      weapon: [],
    };
  },
  methods: {
    addArmor() {
      this.armor.push(this.text);
    },
    remove(num) {
      this.armor.splice(num, 1);
    },
    addWeapon() {
      this.weapon.push(this.weaponname);
    },
    removeWeapon(num) {
      this.weapon.splice(num, 1);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/main.scss";

.helthblock {
  @include flexColumn;
  justify-content: flex-start;
  align-items: center;
  gap: 16px;

  &_firstblock {
    @include flexColumn;
    @include flexstart;
    justify-content: flex-start;
    align-items: flex-start;
    gap: 16px;
    border: 1px solid black;
    border-radius: 12px;
    padding: 8px;

    &_armor {
      @include flexrow;
      justify-content: space-between;
      align-items: flex-start;
      gap: 46px;

      &_leftblock,
      &_middleblock,
      &_rightblock {
        @include flexColumn;
        @include flexcenter;
        gap: 4px;

        &_value {
          width: 60px;
          height: 60px;
          border: 2px solid black;
          border-radius: 12px;
          display: flex;
          justify-content: center;
          align-items: center;
          text-align: center;
        }
      }
    }

    &_helth {
      @include flexColumn;
      @include flexstart;
      gap: 4px;
      border: 2px solid black;
      border-radius: 12px 12px 0 0;
      padding: 6px;

      &_maxhelth {
        @include flexrow;
        justify-content: center;
        align-items: flex-start;
        gap: 4px;

        &_value {
          width: 160px;
          border-radius: 12px;
          text-align: center;
        }
      }

      &_currenthelth {
        width: 290px;
        height: 50px;
        text-align: center;
      }

      &_named {
        margin-left: 70px;
      }
    }

    &_temporhelth {
      border: 2px solid black;
      border-radius: 0 0 12px 12px;
      padding: 6px;

      &_value {
        width: 290px;
        height: 30px;
        text-align: center;
      }
    }

    &_bottomblocks {
      @include flexrow;
      justify-content: center;
      align-items: flex-start;
      gap: 26px;

      &_helthdice {
        @include flexColumn;
        justify-content: center;
        align-items: flex-start;
        gap: 4px;
        border: 2px solid black;
        border-radius: 12px;
        padding: 4px;

        &_total {
          @include flexrow;
          justify-content: flex-start;
          align-items: center;
          gap: 4px;

          &_value {
            width: 65px;
            border-radius: 12px;
            text-align: center;
          }
        }

        &_value {
          width: 100px;
          height: 30px;
          text-align: center;
        }
      }

      &_deathdice {
        @include flexColumn;
        @include flexcenter;
        gap: 8px;
        border: 2px solid black;
        border-radius: 12px;
        padding: 16px 8px;

        &_check {
          &_succes,
          &_fail {
            @include flexrow;
            justify-content: flex-start;
            align-items: center;
            gap: 4px;
          }
        }
      }
    }
  }

  &_secondblock {
    @include flexColumn;
    @include flexstart;
    gap: 8px;
    border: 1px solid black;
    border-radius: 12px;
    padding: 6px;
    height: 331px;
    position: relative;

    &_armor {
      &_text {
        text-align: start;
      }

      &_value {
        border-radius: 12px;
        text-align: center;
      }
    }

    &_weapon {
      @include flexColumn;
      justify-content: center;
      align-items: flex-start;
      gap: 8px;

      &_items {
        @include flexrow;
        justify-content: flex-start;
        align-items: center;
        gap: 4px;

        &_type {
          @include flexColumn;
          @include flexcenter;
          gap: 8px;

          &_text {
            text-align: start;
          }

          &_firstvalue {
            width: 70px;
            border-radius: 12px;
          }

          &_secondvalue {
            width: 40px;
            border-radius: 12px;
          }

          &_thirdvalue {
            width: 70px;
            border-radius: 12px;
          }
        }
      }
    }

    &_blockname {
      margin-left: 70px;
      position: absolute;
      bottom: 6px;
    }
  }
}
</style>
