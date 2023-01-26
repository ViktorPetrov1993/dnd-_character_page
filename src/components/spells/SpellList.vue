<template>
  <div class="main_conteiner textm fw-500">
    Your spells
    <div class="firstrow">
      <div>
        <ul class="textm fw-500">
          0 Circle
          <li>acid arrow</li>
        </ul>
      </div>
      <div>
        <ul class="textm fw-500">
          1 Circle
          <li>acid arrow</li>
        </ul>
        <input type="checkbox" />
      </div>
      <div>
        <ul class="textm fw-500">
          2 Circle
          <li>acid arrow</li>
        </ul>
        <input type="checkbox" />
      </div>
      <div>
        <ul class="textm fw-500">
          4 Circle
          <li>acid arrow</li>
        </ul>
        <input type="checkbox" />
      </div>
      <div>
        <ul class="textm fw-500">
          5 Circle
          <li>acid arrow</li>
        </ul>
        <input type="checkbox" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "spelllist-block",
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
  justify-content: space-between;
}
</style>
