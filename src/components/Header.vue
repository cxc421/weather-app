<template>
  <div class="Header">
    <button class="ripple">
      <img src="../assets/baseline-menu-24px.svg" alt="menu-toggler">
    </button>
    <div class="city-block">
      <h1>臺北市</h1>
      <h2>3:16 下午 CST</h2>
    </div>
    <button class="ripple">
      <img src="../assets/baseline-add-24px.svg" alt="menu-toggler">
    </button>
  </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style lang="scss" scoped>
  .Header {
    display: flex;
    justify-content: space-between;
    position: relative;
    top: 0;
    left: 0;
    z-index: 1;
    flex-shrink: 0;
    padding: 5px 10px;
    margin-left: -10px;
    margin-right: -10px;
    background-color: rgba(0,0,0,0.02);
    background-image: linear-gradient(rgba(0,0,0,0.25), rgba(0,0,0,0.01));
    box-shadow: 0 0 15px 5px rgba(0,0,0,0.01);
    // background: pink;
  }
  button {
    background: transparent;
    outline: none;
    border: none;
    cursor: pointer;

    img {
      height: 28px;
    }
  }
  .city-block {
    text-align: center;
  }
  h1 {
    font-size: 18px;
  }
  h2 {
    font-size: 14px;
  }
</style>
