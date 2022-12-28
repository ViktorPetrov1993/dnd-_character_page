<template>
  <section class="mainblock">
    <div class="firstblock">
      <input type="number" class="smallsquare" />
      <div class="textl fw-700">PASSIVE WISDOM (PERCEPTION)</div>
    </div>
    <div class="secondblock">
      <div>
        <input type="text" v-model="text" class="mediumlargeinput" />
        <button class="button button--info" @click="addTraits">add</button>
      </div>
      <div
        v-for="n of traits"
        :key="'traits' + n"
        @click="removeTraits(n)"
        class="menutextm"
      >
        {{ n }}
      </div>
      <div class="secondblock_blockname menutextm">
        OTHER PROFICIENCIES & LANGUAGES
      </div>
    </div>
    <div class="thirdblock">
      <div>
        <input type="text" v-model="textweapon" class="mediumlargeinput" />
        <button class="button button--info" @click="addWeapon">add</button>
      </div>
      <div class="thirdblock_rowmenu">
        <div>
          <div class="smallbox">
            <div>cp</div>
            <div><input type="number" class="smallsquare" /></div>
          </div>
          <div class="smallbox">
            <div>sp</div>
            <div><input type="number" class="smallsquare" /></div>
          </div>
          <div class="smallbox">
            <div>ep</div>
            <div><input type="number" class="smallsquare" /></div>
          </div>
          <div class="smallbox">
            <div>cp</div>
            <div><input type="number" class="smallsquare" /></div>
          </div>
          <div class="smallbox">
            <div>pp</div>
            <div><input type="number" class="smallsquare" /></div>
          </div>
        </div>
        <div class="">
          <div
            v-for="n of weapon"
            :key="'weapon' + n"
            @click="removeWeapon(n)"
            class="menutextm"
          >
            {{ n }}
          </div>
          <div class="thirdblock_rowmenu_blockname menutextm">EQUIPMENT</div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data() {
    return {
      text: null,
      textweapon: null,
      traits: [],
      weapon: [],
    };
  },
  methods: {
    addTraits() {
      this.traits.push(this.text);
    },
    remove(num) {
      this.traits.splice(num, 1);
    },
    addWeapon() {
      this.weapon.push(this.textweapon);
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
.mainblock {
  @include flexColumn;
  @include flexstart;
  gap: 6px;
}
.firstblock {
  width: 350px;
  @include flexrow;
  @include flexcenter;
  gap: 4px;
  border: 1px solid black;
  border-radius: 12px;
  padding: 10px 8px;
}
.secondblock {
  height: 350px;
  width: 350px;
  @include flexColumn;
  @include flexstart;
  gap: 4px;
  border: 1px solid black;
  border-radius: 12px;
  padding: 10px 8px;
  position: relative;
  overflow-y: hidden;

  &_blockname {
    margin-left: 15px;
    position: absolute;
    bottom: 6px;
  }
}
.thirdblock {
  height: 350px;
  width: 350px;
  @include flexColumn;
  @include flexstart;
  gap: 4px;
  border: 1px solid black;
  border-radius: 12px;
  padding: 10px 8px;
  position: relative;
  overflow-y: hidden;

  &_rowmenu {
    @include flexrow;
    justify-content: space-between;
    align-items: flex-start;
    gap: 6px;
    padding-top: 16px;

    &_blockname {
      margin-left: 15px;
      position: absolute;
      bottom: 6px;
    }
  }
}
.smallbox {
  @include flexrow;
  @include flexcenter;
  gap: 2px;
}
</style>
