<template>
  <div class="app">
    <div class="main">
      <h1>Hello World</h1>
      <p>This is a simple example of a Vue.js component.</p>
    </div>
    <div class="main2">
      <div id="react-app"></div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {},
  mounted() {
    import("react/mountReact").then((mountReact) => {
      mountReact.default();
    });
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  overflow: hidden;
}
.app {
 display: flex;
}
.main {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 50vw;
  height: 100vh;
  background-color: beige;
  border: 1px solid black;
}
.main2 {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 50vw;
  height: 100vh;
  background-color: beige;
}
</style>