<template>
  <div class="app">
    <Header :dark="dark" @toggle-theme="toggleTheme"></Header>
    <Sidebar :dark="dark"></Sidebar>
    <router-view :dark="dark"></router-view>
  </div>
</template>

<script>
// Imports
import Header from "./components/Header.vue";
import Sidebar from "./components/Sidebar.vue";

export default {
  components: {
    Header,
    Sidebar,
  },
  data() {
    return {
      dark: false,
    };
  },
  methods: {
    toggleTheme() {
      this.dark = !this.dark;
    },
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=DM+Sans&family=Merriweather+Sans&family=Poppins:wght@600;700&display=swap");

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "DM Sans";
}

a,
li {
  text-decoration: none;
}

input, textarea {
  background: transparent;
}

*::-webkit-scrollbar {
  width: 3px;
}

/* Track */
*::-webkit-scrollbar-track {
  background: transparent;
}

/* Handle */
*::-webkit-scrollbar-thumb {
  background: rgb(200, 200, 200);
}

img {
  object-fit: cover;
  object-position: center center;
}

a,
button {
  cursor: pointer;
}
</style>
