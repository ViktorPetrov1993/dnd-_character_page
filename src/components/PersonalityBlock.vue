<template>
  <section class="mainblock">
    <div class="mainblock_toppart">
      <div class="firstblock border_firstblock">
        <div class="firstblock_content">
          <input type="text" v-model="texttraits" class="mediumlargeinput" />
          <button class="add" @click="addTraits">add</button>
        </div>
        <div
          v-for="n of traits"
          :key="'traits' + n"
          @click="removeTraits(n)"
          class="menutextm"
        >
          {{ n }}
        </div>
        <div class="firstblock_blockname menutextm">PERSONALITY TRAITS</div>
      </div>
      <div class="secondblock border_secondblock">
        <div class="secondblock_content">
          <input type="text" v-model="textideals" class="mediumlargeinput" />
          <button class="add" @click="addIdeals">add</button>
        </div>
        <div
          v-for="n of ideals"
          :key="'ideals' + n"
          @click="removeIdeals(n)"
          class="menutextm"
        >
          {{ n }}
        </div>
        <div class="secondblock_blockname menutextm">IDEALS</div>
      </div>
      <div class="thirdblock border_thirdblock">
        <div class="thirdblock_content">
          <input type="text" v-model="textbonds" class="mediumlargeinput" />
          <button class="add" @click="addBonds">add</button>
        </div>
        <div
          v-for="n of bonds"
          :key="'bonds' + n"
          @click="removeBonds(n)"
          class="menutextm"
        >
          {{ n }}
        </div>
        <div class="thirdblock_blockname menutextm">BONDS</div>
      </div>
      <div class="fourthblock border_fourthblock">
        <div class="fourthblock_content">
          <input type="text" v-model="textflaws" class="mediumlargeinput" />
          <button class="add" @click="addFlaws">add</button>
        </div>
        <div
          v-for="n of flaws"
          :key="'flaws' + n"
          @click="removeFlaws(n)"
          class="menutextm"
        >
          {{ n }}
        </div>
        <div class="fourthblock_blockname menutextm">FLAWS</div>
      </div>
    </div>
    <div class="mainblock_bottompart fivethblock">
      <div class="fivethblock_contant">
        <input type="text" class="mediumlargeinput" v-model="text" />
        <button class="add" @click="addTodo">add</button>
      </div>
      <div
        v-for="n of todos"
        :key="'item' + n"
        @click="remove(n)"
        class="menutextm"
      >
        {{ n }}
      </div>
      <div class="fivethblock_blockname menutextm">FEATURES & TRAITS</div>
    </div>
  </section>
</template>

<script>
export default {
  name: "PersonalityBlock-comp",
  props: {
    msg: String,
  },
  data() {
    return {
      text: null,
      texttraits: null,
      textideals: null,
      textbonds: null,
      textflaws: null,
      todos: [],
      traits: [],
      ideals: [],
      bonds: [],
      flaws: [],
    };
  },
  methods: {
    addTodo() {
      this.todos.push(this.text);
    },
    remove(num) {
      this.todos.splice(num, 1);
    },
    addTraits() {
      this.traits.push(this.texttraits);
    },
    removeTraits(num) {
      this.traits.splice(num, 1);
    },
    addIdeals() {
      this.ideals.push(this.textideals);
    },
    removeIdeals(num) {
      this.ideals.splice(num, 1);
    },
    addBonds() {
      this.bonds.push(this.textbonds);
    },
    removeBonds(num) {
      this.bonds.splice(num, 1);
    },
    addFlaws() {
      this.flaws.push(this.textflaws);
    },
    removeFlaws(num) {
      this.flaws.splice(num, 1);
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

  &_toppart {
    @include flexColumn;
    @include flexstart;
    gap: 6px;
  }
}
.firstblock,
.secondblock,
.thirdblock,
.fourthblock,
.fivethblock {
  @include flexColumn;
  @include flexstart;
  gap: 6px;
  position: relative;
  overflow-y: hidden;
  width: 300px;

  &_content {
    @include flexrow;
    @include flexcenter;
    gap: 4px;
  }
  &_blockname {
    position: absolute;
    bottom: 6px;
    left: 42px;
  }
}
.mainblock_bottompart {
  @include flexColumn;
  @include flexstart;
  gap: 4px;
  border: 1px solid black;
  border-radius: 12px;
  position: relative;
  height: 320px;
}
.border_firstblock {
  border: 1px solid black;
  border-radius: 12px 12px 0 0;
  height: 125px;
}
.border_secondblock,
.border_thirdblock {
  border: 1px solid black;
  height: 100px;
}
.border_fourthblock {
  border: 1px solid black;
  border-radius: 0 0 12px 12px;
  height: 125px;
}
</style>
