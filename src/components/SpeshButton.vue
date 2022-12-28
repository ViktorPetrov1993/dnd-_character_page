<!-- <template>
  <button
    @click="emitText"
    :class="[
      'button',
      { 'button--primary': isPrimary },
      { 'button--secondary': isSecondary },
      { 'button--danger': isDanger },
    ]"
  >
    BUTTON TO TEST
  </button>
  <div v-for="n in testdata" :key="n">{{ n.Description }}</div>
</template>

<script>
export default {
  name: "theme-button",
  //   props: [
  //     "isPrimary",
  //     "isSecondary",
  //     "isDanger",
  //     "isSucess",
  //     "isWarning",
  //     "isInfo",
  //   ],
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
      fetch("https://api.publicapis.org/entries")
        .then((response) => {
          return response.json();
        })
        .then((data) => {
          console.log("ЧИСТЫЕ ДАННЫЕ С СЕРВЕРА: ", data);
          this.testdata = data.entries;
        });
    },
  },
};
</script> -->
