<template>
  <div class="main_conteiner textm fw-500">
    Your abilitys
    <div class="firstrow"></div>
  </div>
</template>

<script>
export default {
  name: "abilitylist-block",
};
</script>

<style scoped lang="scss">
@import "../../assets/scss/main.scss";

.main_conteiner {
  border: 1px solid $border-color;
  border-radius: 12px;
  width: 98%;
  height: 100%;
  padding: 5px;
  margin: 5px;
  padding-left: 15px;
}
.firstrow {
  @include flexrow;
  justify-content: flex-start;
  align-items: flex-start;
}
</style>
