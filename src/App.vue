<template>
  <div id="app">
    <div class="tab-bar-wrapper">
      <md-tab-bar class="tab-bar" v-model="current" :items="items" />
    </div>
  </div>
</template>

<script>
import { TabBar } from "mand-mobile";

export default {
  name: "app",
  components: {
    [TabBar.name]: TabBar
  },
  data() {
    return {
      current: 2,
      items: [{ name: 1, label: "标签标签" }, { name: 2, label: "标签标签" }]
    };
  }
};
</script>
<style lang="stylus">
@import '~minireset.css/minireset.css';
@import '~mand-mobile/lib-vw/mand-mobile.css';

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.tab-bar-wrapper {
  margin: 4.27vw;
}

.tab-bar {
  padding: 0;
  width: 50%;
  background-color: #00f0f0;
}

.tab-bar .md-tab-bar-item {
  font-size: 3.73333 * 1.4 vw;
}
</style>
