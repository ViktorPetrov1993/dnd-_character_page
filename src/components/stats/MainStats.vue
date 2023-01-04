<template>
  <section>
    <div class="stats_main">
      <div>
        <div class="textl fw-700">{{ stat_name }}</div>
        <input
          type="number"
          v-model="localModel"
          @input="handleUpdate"
          class="squareinput textxxl"
        />
      </div>
      <div class="stats_main_value textl">{{ modifier }}</div>
    </div>
  </section>
</template>

<script>
export default {
  name: "mainStats-comp",
  emits: ["update:stat_value"],

  props: {
    stat_name: String,
    stat_value: Number,
    stat_modifier: Number,
  },
  data() {
    return {
      localModel: 10,
    };
  },
  mounted() {
    this.localModel = this.stat_value;
  },
  computed: {
    modifier() {
      return Math.floor((this.stat_value - 10) / 2);
    },
  },
  methods: {
    handleUpdate() {
      this.$emit("update:stat_value", this.localModel);
    },
  },
};
</script>

<style scoped lang="scss">
@import "../../assets/scss/main.scss";

.stats_main {
  @include flexColumn;
  @include flexcenter;
  gap: 4px;
}
</style>
