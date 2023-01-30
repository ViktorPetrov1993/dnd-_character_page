<template>
  <div class="textm fw-500">
    {{ spell }}
  </div>
</template>

<script>
export default {
  name: "spell-page",
  data() {
    return {
      spell: null,
    };
  },

  created() {
    this.getSpells();
  },
  methods: {
    getSpells() {
      fetch(`https://www.dnd5eapi.co/api/spells/${this.$route.params.spell}`)
        .then((response) => {
          return response.json();
        })
        .then((data) => {
          this.spell = data;
        });
    },
  },
};
</script>
