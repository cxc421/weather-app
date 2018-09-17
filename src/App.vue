<template>
  <div id="app">
    <div
      v-show="isLoading"
      id="loading-icon"
      class="lds-dual-ring"></div>
    <main
      v-show="!isLoading"
    >
      <div
        class="bg-scence"
        :style="bgStyle"></div>
      <Header />
      <div
        class="content"
        @scroll="onContentScroll"
      >
        <div class="summary-section">
          <Summary />
        </div>
      </div>
    </main>
  </div>
</template>

<script>
import bgImage from './assets/bg-images/clear-night.jpg'
import Header from './components/Header'
import Summary from './components/Summary'

const bgMaxScrollHeight = 120

export default {
  name: 'app',
  components: {
    Header,
    Summary
  },
  data () {
    return {
      isLoading: false,
      scrollTop: 0
    }
  },
  computed: {
    bgStyle () {
      return {
        backgroundImage: `url('${bgImage}')`,
        height: `calc(100% + ${bgMaxScrollHeight}px)`,
        top: `-${this.scrollTop}px`
      }
    }
  },
  methods: {
    onContentScroll (evt) {
      const val = evt.target.scrollTop / 4
      if (val < bgMaxScrollHeight) {
        this.scrollTop = val
      }
    }
  }
}
</script>

<style lang="scss">
@import url('./assets/styles/loader.css');
@import url('./assets/styles/ripple.css');

*, *::before, *::after {
  box-sizing: border-box;
}

body, html {
  padding: 0;
  margin: 0;
  height: 100%;
  background: #eee;
  color: white;
  user-select: none;
}

h1, h2, h3, h4, h5, h6, p {
  margin: 0;
}

#app {
  font-family: 'Avenir', Microsoft JhengHei, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  // max-width: 376px;
  // max-height: 668px;
  height: 100%;
  width: 100%;
  background: white;
  position: relative;
  // top: 50%;
  // left: 50%;
  // transform: translate(-50%, -50%);
}

#loading-icon {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

main {
  position: relative;
  width: 100%;
  height: 100%;
  padding: 0 10px;
  overflow: hidden;

  display: flex;
  flex-direction: column;
}

.bg-scence {
  position: absolute;
  left: 0;
  width: 100%;
  // background: lightseagreen;
  background-size: cover;

  height: calc(100% + 50px);
  top: 0;

  z-index: 0;
}

.content {
  // background-color: skyblue;
  flex-grow: 1;
  overflow: auto;
  position: relative;
  z-index: 1;

  &::-webkit-scrollbar {
    display: none;
  }
}

.summary-section {
  height: calc(100vh - 56px);
  // background-color: yellow;
  position: relative;
}

.test {
  // background-color: yellow;
  width: 100px;
  height: 2000px;
}
</style>
