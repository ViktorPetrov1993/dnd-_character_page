<template>
  <section class="">
    <div class="header">
      <div class="header_rightpart">
        <div class="header_rightpart-textwithbtn">
          <input type="text" class="input" />
          <button class="add">add</button>
        </div>
        <div class="menutextl">CHARACTER NAME</div>
      </div>
      <div class="header_leftpart">
        <div class="firstrow">
          <div class="firstrow_content">
            <div class="firstrow_content-textwithbtn">
              <select class="select" name="CLASS" id="">
                <option value="Barbarian">Barbarian</option>
                <option value="Barbarian">Barbarian</option>
                <option value="Barbarian">Barbarian</option>
                <option value="Barbarian">Barbarian</option>
              </select>
              <button class="add">add</button>
            </div>
            <div class="menutextl">CLASS</div>
          </div>
          <div class="firstrow_content">
            <div class="firstrow_content-textwithbtn">
              <select class="select" name="CLASS" id="">
                <option value="Barbarian">Barbarian</option>
                <option value="Barbarian">Barbarian</option>
                <option value="Barbarian">Barbarian</option>
                <option value="Barbarian">Barbarian</option>
              </select>
              <button class="add">add</button>
            </div>
            <div class="menutextl">BACKGROUND</div>
          </div>
          <div class="firstrow_content">
            <div class="firstrow_content-textwithbtn">
              <input type="text" class="smallinput" />
              <button class="add">add</button>
            </div>
            <div class="menutextl">PLAYER NAME</div>
          </div>
        </div>
        <div class="secondrow">
          <div class="firstrow_content">
            <div class="firstrow_content-textwithbtn">
              <select class="select" name="CLASS" id="">
                <option value="Barbarian">Barbarian</option>
                <option value="Barbarian">Barbarian</option>
                <option value="Barbarian">Barbarian</option>
                <option value="Barbarian">Barbarian</option>
              </select>
              <button class="add">add</button>
            </div>
            <div class="menutextl">RACE</div>
          </div>
          <div class="firstrow_content">
            <div class="firstrow_content-textwithbtn">
              <select class="select" name="CLASS" id="">
                <option value="Barbarian">Barbarian</option>
                <option value="Barbarian">Barbarian</option>
                <option value="Barbarian">Barbarian</option>
                <option value="Barbarian">Barbarian</option>
              </select>
              <button class="add">add</button>
            </div>
            <div class="menutextl">ALIGNMENT</div>
          </div>
          <div class="firstrow_content">
            <div class="firstrow_content-textwithbtn">
              <input type="text" class="smallinput" />
              <button class="add">add</button>
            </div>
            <div class="menutextl">EXPERIENCE POINTS</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/main.scss";

.header {
  @include flexrow;
  justify-content: space-between;
  align-items: center;
  padding: 4px;

  &_rightpart {
    @include flexColumn;
    justify-content: center;
    align-items: flex-start;
    gap: 4px;
    padding: 12px;
    border: 1px solid black;
    border-radius: 12px;

    &_textwithbtn {
      @include flexrow;
      gap: 4px;
    }
  }

  &_leftpart {
    @include flexColumn;
    @include flexcenter;
    border: 1px solid black;
    padding: 12px;
    border-radius: 12px;
  }
  .firstrow,
  .secondrow {
    display: flex;
    flex-flow: row wrap;
    @include flexcenter;
    gap: 4px;

    &_content {
      @include flexColumn;
      justify-content: center;
      align-items: flex-start;
      gap: 4px;

      &_-textwithbtn {
        @include flexrow;
        gap: 4px;
      }
    }
  }
  .menutextl {
    border-top: 1px solid black;
    width: 98%;
    text-align: start;
    padding: 4px;
    color: crimson;
  }
}
</style>
