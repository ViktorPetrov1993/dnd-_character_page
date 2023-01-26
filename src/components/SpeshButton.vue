<template>
  <!-- <button
    @click="emitText"
    :class="[
      'button',
      { 'button--primary': isPrimary },
      // { 'button--secondary': isSecondary },
      { 'button--danger': isDanger },
    ]"
  >
    BUTTON TO TEST
  </button> -->
  <div class="textm" v-for="n in testdata" :key="n">{{ n }}</div>
</template>

<script>
export default {
  name: "theme-button",
  // props: [
  //   "isPrimary",
  //   "isSecondary",
  // "isDanger",
  //   //     "isSucess",
  //   //     "isWarning",
  //   //     "isInfo",
  // ],
  props: {
    isPrimary: Boolean,
    isDanger: Boolean,
  },
  data() {
    return {
      testdata: null,
    };
  },
  mounted() {
    this.getItems();
  },
  methods: {
    emitText() {
      this.$emit(
        "testEvent",
        "sddgijshjfoglknsdoifjgnspdfokgspodknfgposdfkngposdngijsnfdg"
      );
    },
    getItems() {
      fetch("https://www.dnd5eapi.co/api/spells/aid")
        .then((response) => {
          return response.json();
        })
        .then((data) => {
          console.log("ЧИСТЫЕ ДАННЫЕ С СЕРВЕРА: ", data);
          this.testdata = data.desc;
        });
    },
  },
};
</script>
