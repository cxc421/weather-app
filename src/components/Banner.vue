<template>
  <div class="banner">
    <div class="summary">
      <div></div>
      <div>
        <span class="boundary-degree-box">
          <img src="../assets/baseline-vertical_align_top-24px.svg" alt="">
          <span>34&#176;</span>
        </span>
        <span class="boundary-degree-box">
          <img src="../assets/baseline-vertical_align_bottom-24px.svg" alt="">
          <span>27&#176;</span>
        </span>
      </div>
      <div class="current-degree">
        33&#176;
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Banner'
}
</script>

<style lang="scss" scoped>
  .banner {
    height: 100vh;
    position: relative;
  }
  .summary {
    position: absolute;
    bottom: 10px;
  }
  .boundary-degree-box {
    margin-right: 20px;
    display: inline-flex;
    align-items: center;

    img {
      height: 24px;
    }

    span {
      font-size: 22px;
    }
  }
  .current-degree {
    font-size: 130px;
    line-height: 130px;
    overflow: hidden;
  }
</style>
