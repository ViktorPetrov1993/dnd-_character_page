<template>
  <section class="mainblock">
    <div class="firstblock">
      <div class="firstblock_bigsqures">
        <div class="firstblock_bigsqures-left">
          <div class="textxxl squareblock">16</div>
          <div class="textl">
            ARMOR <br />
            CLASS
          </div>
        </div>
        <div class="firstblock_bigsqures-middle">
          <input type="text" class="squareinput textxxl" />
          <div class="textl">INITIATIVE</div>
        </div>
        <div class="firstblock_bigsqures-right">
          <div class="textxxl squareblock">35</div>
          <div class="textl">SPEED</div>
        </div>
      </div>
      <div class="firstblock_inputblocks">
        <div class="firstblock_inputblocks-textwithbtn">
          <div class="textm">Hit Point Max</div>
          <input type="number" class="smallsquare" />
        </div>
        <input type="text" class="biginput textxxl" />
        <div class="firstblock_blockname textm">CURRENT HIT POINTS</div>
      </div>
      <div class="firstblock_reversinputblocks">
        <input type="text" class="biginput textxxl" />
        <div class="textm">TEMPORARY HIT POINTS</div>
      </div>
      <div class="firstblock_bottomblocks">
        <div class="leftpart">
          <div class="leftpart-withsmallinput">
            <div class="textll">Total</div>
            <input type="text" class="verysmallinput" />
          </div>
          <input type="text" class="mediuminput" />
          <div class="textlx">HIT DICE</div>
        </div>
        <div class="firstblock_bottomblocks">
          <div class="rightpart">
            <label for="succes" class="rightpart-radio"
              ><div class="textlx">SUCCESSES</div>
              <input type="checkbox" v-for="n of 3" :key="'succes' + n" />{{
                n
              }}
            </label>
            <label class="rightpart-radio"
              ><div class="textlx">FAILURES</div>
              <input
                type="checkbox"
                v-model="deathSaves"
                v-for="n of 3"
                :key="'fail' + n"
                :value="n"
              />{{ n }}
            </label>
            <div class="textlx">DEATH SAVES</div>
          </div>
        </div>
      </div>
    </div>
    <div class="secondblock">
      <div class="secondblock_toppart">
        <div>
          <div class="textm">ARMOR</div>
          <select name="" id="" class="select">
            <option value="Barbarian">Barbarian</option>
            <option value="Barbarian">Barbarian</option>
            <option value="Barbarian">Barbarian</option>
            <option value="Barbarian">Barbarian</option>
          </select>
        </div>
      </div>
      <div class="secondblock_bottompart">
        <div class="secondblock_bottompart-rowinputs">
          <div class="textm">NAME</div>
          <div class="textm">ATK BONUS</div>
          <div class="textm">DAMAGE/TYPE</div>
        </div>
        <div class="secondblock_bottompart-rowinputs">
          <div class="">
            <input
              type="text"
              v-model="weaponname"
              class="mediumlargeinput"
              multiple="3"
            />
          </div>
          <button class="button button--info" @click="addWeapon">add</button>
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
      <div class="secondblock_blockname textm">ATTACKS & SPELLCASTING</div>
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
      weapon: [],
      weaponname: null,
      deathSaves: [],
    };
  },
  methods: {
    addWeapon() {
      this.weapon.push(this.weaponname);
    },
    removeWeapon(num) {
      this.weapon.splice(num, 1);
    },
  },
  watch: {
    deathSaves() {
      if (this.deathSaves.length > 2) {
        alert("U ARE DEAD");
      }
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../assets/scss/main.scss";
.mainblock {
  @include flexColumn;
  justify-content: flex-start;
  align-items: center;
  gap: 12px;
}
.firstblock {
  @include flexColumn;
  @include flexstart;
  justify-content: flex-start;
  align-items: flex-start;
  gap: 16px;
  border: 1px solid $border-color;
  border-radius: 12px;
  padding: 8px;

  &_bigsqures {
    @include flexrow;
    justify-content: space-between;
    align-items: flex-start;
    gap: 41px;

    &_left,
    &_middle,
    &_right {
      @include flexColumn;
      @include flexcenter;
      gap: 4px;
    }
  }

  &_inputblocks {
    @include flexColumn;
    @include flexstart;
    gap: 4px;
    border: 2px solid $border-color;
    border-radius: 12px 12px 0 0;
    padding: 6px;

    &-textwithbtn {
      @include flexrow;
      @include flexcenter;
      gap: 4px;
    }
  }

  &_reversinputblocks {
    border: 2px solid $border-color;
    border-radius: 0 0 12px 12px;
    padding: 6px;
  }

  &_bottomblocks {
    @include flexrow;
    justify-content: center;
    align-items: flex-start;
    gap: 4px;
  }
}
.leftpart {
  @include flexColumn;
  justify-content: center;
  align-items: flex-start;
  gap: 4px;
  border: 2px solid $border-color;
  border-radius: 12px;
  padding: 10px 4px;

  &-withsmallinput {
    @include flexrow;
    justify-content: flex-start;
    align-items: center;
    gap: 4px;
  }
}
.rightpart {
  @include flexColumn;
  @include flexcenter;
  gap: 8px;
  border: 2px solid $border-color;
  border-radius: 12px;
  padding: 13px 8px;

  &-radio {
    @include flexrow;
    justify-content: flex-start;
    align-items: center;
  }
}
.secondblock {
  @include flexColumn;
  @include flexstart;
  gap: 4px;
  border: 1px solid $border-color;
  border-radius: 12px;
  padding: 6px;
  height: 312px;
  width: 318px;
  position: relative;
  overflow-y: hidden;

  &_bottompart {
    @include flexColumn;
    justify-content: center;
    align-items: flex-start;
    gap: 8px;
    &-rowinputs {
      @include flexrow;
      justify-content: flex-start;
      align-items: center;
      gap: 4px;
    }
  }

  &_blockname {
    margin-left: 70px;
    position: absolute;
    bottom: 6px;
  }
}
.squareblock {
  width: 60px;
  min-height: 70px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
