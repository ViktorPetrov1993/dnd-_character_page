<template>
  <div class="img_conteiner">
    <div class="textl fw-700">Download your character img</div>
  </div>
</template>

<script>
export default {
  name: "characterimg-block",
};
</script>

<style scoped lang="scss">
@import "../assets/scss/main.scss";

.img_conteiner {
  height: 814px;
  width: 419px;
  border: 1px solid $border-color;
  border-radius: 12px;
  background-position: center !important;
  background-repeat: no-repeat !important;
  background-size: cover !important;
  @include flexColumn;
  justify-content: flex-start;
  align-items: center;
  background: url(../assets/img/character_img.jpg);
}
</style>
