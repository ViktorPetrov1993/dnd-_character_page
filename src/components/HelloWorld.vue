<template>
  <section class="header">
    <div class="header_content">
      <div class="header_content_rightpart">
        <div class="header_content_rightpart_textwithbtn">
          <input type="text" class="textinput" />
          <button class="add">add</button>
        </div>
        <div class="menutextl">CHARACTER NAME</div>
      </div>
      <div class="header_content_leftpart">
        <div class="header_content_leftpart_rowblock">
          <div class="header_content_leftpart_rowblock_textfiled">
            <div class="header_content_leftpart_rowblock_textfiled_textwithbtn">
              <input type="text" class="textinput" />
              <button class="add">add</button>
            </div>
            <div class="menutextl">CLASS & LEVEL</div>
          </div>
          <div class="header_content_leftpart_rowblock_textfiled">
            <div class="header_content_leftpart_rowblock_textfiled_textwithbtn">
              <input type="text" class="textinput" />
              <button class="add">add</button>
            </div>
            <div class="menutextl">BACKGROUND</div>
          </div>
          <div class="header_content_leftpart_rowblock_textfiled">
            <div class="header_content_leftpart_rowblock_textfiled_textwithbtn">
              <input type="text" class="textinput" />
              <button class="add">add</button>
            </div>
            <div class="menutextl">PLAYER NAME</div>
          </div>
        </div>
        <div class="header_content_leftpart_rowblock">
          <div class="header_content_leftpart_rowblock_textfiled">
            <div class="header_content_leftpart_rowblock_textfiled_textwithbtn">
              <input type="text" class="textinput" />
              <button class="add">add</button>
            </div>
            <div class="menutextl">RACE</div>
          </div>
          <div class="header_content_leftpart_rowblock_textfiled">
            <div class="header_content_leftpart_rowblock_textfiled_textwithbtn">
              <input type="text" class="textinput" />
              <button class="add">add</button>
            </div>
            <div class="menutextl">ALIGNMENT</div>
          </div>
          <div class="header_content_leftpart_rowblock_textfiled">
            <div class="header_content_leftpart_rowblock_textfiled_textwithbtn">
              <input type="text" class="textinput" />
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

.header_content {
  display: flex;
  flex-flow: row;
  justify-content: space-between;
  align-items: center;
  padding: 4px;

  &_rightpart {
    display: flex;
    flex-flow: column;
    justify-content: center;
    align-items: flex-start;
    gap: 4px;
    border: 1px solid black;
    padding: 8px;
    border-radius: 12px 0 0 12px;
    border-right: none;
    width: 65%;

    &_textwithbtn {
      display: flex;
      flex-flow: row;
      gap: 4px;
    }
  }

  &_leftpart {
    display: flex;
    flex-flow: column;
    justify-content: center;
    align-items: center;
    max-width: 700px;
    border: 1px solid black;
    padding: 8px;
    border-radius: 12px;

    &_rowblock {
      display: flex;
      flex-flow: row wrap;
      justify-content: center;
      align-items: center;
      gap: 4px;

      &_textfiled {
        display: flex;
        flex-flow: column;
        justify-content: center;
        align-items: flex-start;
        gap: 4px;
        width: 30%;

        &_textwithbtn {
          display: flex;
          flex-flow: row;
          gap: 4px;
        }
      }
    }
  }
  .textinput {
    width: 90%;
    border-radius: 12px;
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
