<template>
  <section class="personality">
    <div class="personality_firstblock">
      <div class="personality_firstblock_traits border_traits">
        <div class="personality_firstblock_traits_content">
          <input
            type="text"
            v-model="texttraits"
            class="personality_firstblock_traits_content_value"
          />
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
        <div class="personality_firstblock_traits_text menutextm">
          PERSONALITY TRAITS
        </div>
      </div>
      <div class="personality_firstblock_ideals border_ideals">
        <div class="personality_firstblock_ideals_content">
          <input
            type="text"
            class="personality_firstblock_ideals_content_value"
          />
          <button class="add">add</button>
        </div>
        <div class="menutextm"></div>
        <div class="personality_firstblock_ideals_text menutextm">IDEALS</div>
      </div>
      <div class="personality_firstblock_bonds border_bonds">
        <div class="personality_firstblock_bonds_content">
          <input
            type="text"
            class="personality_firstblock_bonds_content_value"
          />
          <button class="add">add</button>
        </div>
        <div class="menutextm"></div>
        <div class="personality_firstblock_ideals_text menutextm">BONDS</div>
      </div>
      <div class="personality_firstblock_flaws border_flaws">
        <div class="personality_firstblock_flaws_content">
          <input
            type="text"
            class="personality_firstblock_flaws_content_value"
          />
          <button class="add">add</button>
        </div>
        <div class="menutextm"></div>
        <div class="personality_firstblock_flaws_text menutextm">FLAWS</div>
      </div>
    </div>
    <div class="personality_secondblock">
      <div class="personality_secondblock_features">
        <input
          type="text"
          class="personality_secondblock_features_value"
          v-model="text"
        />
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
      <div class="personality_secondblock_blockname menutextm">
        FEATURES & TRAITS
      </div>
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
      todos: [],
      traits: [],
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
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/main.scss";

.personality {
  display: flex;
  flex-flow: column;
  justify-content: flex-start;
  align-items: flex-start;
  gap: 6px;

  &_firstblock {
    display: flex;
    flex-flow: column;
    justify-content: flex-start;
    align-items: flex-start;
    gap: 6px;

    &_traits,
    &_ideals,
    &_bonds,
    &_flaws {
      display: flex;
      flex-flow: column;
      justify-content: flex-start;
      align-items: flex-start;
      gap: 6px;
      position: relative;

      &_content {
        display: flex;
        flex-flow: row;
        justify-content: center;
        align-items: center;
        gap: 4px;

        &_value {
          border-radius: 12px;
          margin: 6px;
        }
      }

      &_text {
        position: absolute;
        bottom: 6px;
        left: 35px;
      }
    }
  }

  &_secondblock {
    display: flex;
    flex-flow: column;
    justify-items: flex-start;
    align-items: flex-start;
    gap: 4px;
    border: 1px solid black;
    border-radius: 12px;
    position: relative;
    height: 320px;

    &_features {
      display: flex;
      flex-flow: row;
      justify-content: center;
      align-items: center;
      gap: 4px;

      &_value {
        margin: 6px;
        border-radius: 12px;
      }
    }

    &_blockname {
      position: absolute;
      bottom: 6px;
      left: 42px;
    }
  }
}
.border_traits {
  border: 1px solid black;
  border-radius: 12px 12px 0 0;
  height: 125px;
}
.border_ideals {
  border: 1px solid black;
  height: 100px;
}
.border_bonds {
  border: 1px solid black;
  height: 100px;
}
.border_flaws {
  border: 1px solid black;
  border-radius: 0 0 12px 12px;
  height: 125px;
}
</style>
