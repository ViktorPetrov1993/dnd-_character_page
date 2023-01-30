<template>
  <div class="main_conteiner textm fw-500">
    Your spells
    <!-- <ul class="textm fw-500">
      <li v-for="(spell, index) in spells" :key="`spell${index}`">
        {{ spell }}
      </li>
    </ul> -->
  </div>
</template>

<script>
export default {
  name: "spelllist-block",
  data() {
    return {
      spells: [],
      url: "https://www.dnd5eapi.co/api/spells/",
    };
  },
  mounted() {
    this.getSpellList();
  },
  methods: {
    getSpellList() {
      fetch(this.url)
        .then((response) => {
          return response.json();
        })
        .then((data) => {
          this.spells = data.results;
        });
    },
  },
};
</script>

<style scoped lang="scss">
@import "../../assets/scss/main.scss";
</style>
