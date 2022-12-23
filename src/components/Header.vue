<template>
  <header :class="{ dark: dark }">
    <div class="logo">Pyxis</div>
    <div class="user">
      <select class="theme-select" @change="$emit('toggle-theme')">
        <option>Light</option>
        <option>Dark</option>
      </select>
      <span>Temurmalik React</span>
      <img src="../assets/img/avatar-small.jpg" alt="" />
    </div>
  </header>
</template>
<script>
export default {
  name: "Header",
  props: ["dark"],
  data() {
    return {};
  },
  methods: {},
};
</script>
<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  box-shadow: 0 0 5px rgb(50, 50, 50);
  padding: 0 25px 0 50px;
  height: 65px;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1;
  border-bottom: 1px solid rgb(245, 245, 245);
  background: #fff;
}

header.dark {
  background: #000;
  color: #fff;
}

.logo {
  font-size: 25px;
  font-weight: 600;
}

.logo img {
  width: 75px;
}

.theme-select {
  border: 1px solid #000;
  border-radius: 0;
  width: 99px;
  border-radius: 0;
  font-size: 15px;
}

.theme-select option {
  width: 50px;
}

.theme-select:focus {
  outline: none;
}

.user {
  display: flex;
  align-items: center;
}

.user img {
  width: 55px;
  height: 55px;
  border-radius: 100%;
}

.user span {
  margin: 0 15px;
}
</style>
