<template>
  <div>
    <input type="text" v-model="search" placeholder="Search spell..." />
    <ul v-if="testdata == !null">
      <li v-for="testdata in filteredList" :key="testdata">
        {{ n.index }}
      </li>
    </ul>
  </div>
  <router-link
    :to="'/spell/' + n.index"
    class="textm"
    v-for="n in testdata"
    :key="n"
    >{{ n.index }}</router-link
  >
</template>

<script>
export default {
  name: "theme-button",
  data() {
    return {
      testdata: null,
      search: "",
    };
  },
  beforeMount() {
    this.getSpells();
  },
  computed: {
    filteredList() {
      return this.testdata.filter((testdata) => {
        return testdata.index.indexOf(this.search) > -1;
      });
    },
  },
  methods: {
    getSpells() {
      fetch("https://www.dnd5eapi.co/api/spells")
        .then((response) => {
          return response.json();
        })
        .then((data) => {
          console.log("ЧИСТЫЕ ДАННЫЕ С СЕРВЕРА: ", data);
          this.testdata = data.results;
        });
    },
  },
};
</script>
