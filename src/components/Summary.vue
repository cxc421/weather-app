<template>
  <div class="summary">
    <div class="weather-summary-row">
      <img src="../assets/summary-icons/cloudy-white.png" >
      <div>多雲</div>
    </div>
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
</template>

<script>
export default {
  name: 'Summary'
}
</script>

<style lang="scss" scoped>
  .summary {
    position: absolute;
    bottom: 10px;
    padding-left: 10px;
    & > div {
      margin-bottom: 6px;
      display: flex;
      align-items: center;
      &:last-child {
        margin-bottom: 0;
      }
    }
  }
  .weather-summary-row {
    img {
      height: 36px;
      margin-right: 6px;
    }
    div {
      font-size: 22px;
      margin-bottom: -4px;
    }
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
    line-height: 110px;
    overflow: hidden;
  }
</style>
