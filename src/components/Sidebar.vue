<template>
  <aside :class="{ dark: dark }">
    <nav class="nav">
      <div class="nav__item">
        <router-link to="/">
          <svg
            viewBox="0 0 24 24"
            aria-hidden="true"
            class="r-18jsvk2 r-4qtqp9 r-yyyyoo r-lwhw9o r-dnmrzs r-bnwqim r-1plcrui r-lrvibr r-cnnz9e"
          >
            <g>
              <path
                d="M12 9c-2.209 0-4 1.791-4 4s1.791 4 4 4 4-1.791 4-4-1.791-4-4-4zm0 6c-1.105 0-2-.895-2-2s.895-2 2-2 2 .895 2 2-.895 2-2 2zm0-13.304L.622 8.807l1.06 1.696L3 9.679V19.5C3 20.881 4.119 22 5.5 22h13c1.381 0 2.5-1.119 2.5-2.5V9.679l1.318.824 1.06-1.696L12 1.696zM19 19.5c0 .276-.224.5-.5.5h-13c-.276 0-.5-.224-.5-.5V8.429l7-4.375 7 4.375V19.5z"
              ></path>
            </g>
          </svg>
          <span>Home</span>
        </router-link>
      </div>
      <div class="nav__item">
        <router-link to="/explore">
          <svg
            viewBox="0 0 24 24"
            aria-hidden="true"
            class="r-18jsvk2 r-4qtqp9 r-yyyyoo r-lwhw9o r-dnmrzs r-bnwqim r-1plcrui r-lrvibr r-cnnz9e"
          >
            <g>
              <path
                d="M10.09 3.098L9.72 7h5.99l.39-4.089 1.99.187L17.72 7h3.78v2h-3.97l-.56 6h3.53v2h-3.72l-.38 4.089-1.99-.187.36-3.902H8.78l-.38 4.089-1.99-.187L6.77 17H2.5v-2h4.46l.56-6H3.5V7h4.21l.39-4.089 1.99.187zM14.96 15l.56-6H9.53l-.56 6h5.99z"
              ></path>
            </g>
          </svg>
          <span>Explore</span>
        </router-link>
      </div>
      <div class="nav__item">
        <router-link to="/notifications">
          <svg
            viewBox="0 0 24 24"
            aria-hidden="true"
            class="r-18jsvk2 r-4qtqp9 r-yyyyoo r-lwhw9o r-dnmrzs r-bnwqim r-1plcrui r-lrvibr r-cnnz9e"
          >
            <g>
              <path
                d="M19.993 9.042C19.48 5.017 16.054 2 11.996 2s-7.49 3.021-7.999 7.051L2.866 18H7.1c.463 2.282 2.481 4 4.9 4s4.437-1.718 4.9-4h4.236l-1.143-8.958zM12 20c-1.306 0-2.417-.835-2.829-2h5.658c-.412 1.165-1.523 2-2.829 2zm-6.866-4l.847-6.698C6.364 6.272 8.941 4 11.996 4s5.627 2.268 6.013 5.295L18.864 16H5.134z"
              ></path>
            </g>
          </svg>
          <span>Nortifications</span>
        </router-link>
      </div>
      <div class="nav__item">
        <router-link to="/messages">
          <svg
            viewBox="0 0 24 24"
            aria-hidden="true"
            class="r-18jsvk2 r-4qtqp9 r-yyyyoo r-lwhw9o r-dnmrzs r-bnwqim r-1plcrui r-lrvibr r-cnnz9e"
          >
            <g>
              <path
                d="M1.998 5.5c0-1.381 1.119-2.5 2.5-2.5h15c1.381 0 2.5 1.119 2.5 2.5v13c0 1.381-1.119 2.5-2.5 2.5h-15c-1.381 0-2.5-1.119-2.5-2.5v-13zm2.5-.5c-.276 0-.5.224-.5.5v2.764l8 3.638 8-3.636V5.5c0-.276-.224-.5-.5-.5h-15zm15.5 5.463l-8 3.636-8-3.638V18.5c0 .276.224.5.5.5h15c.276 0 .5-.224.5-.5v-8.037z"
              ></path>
            </g>
          </svg>
          <span>Messages</span>
        </router-link>
      </div>
      <div class="nav__item">
        <router-link to="/bookmarks">
          <svg
            viewBox="0 0 24 24"
            aria-hidden="true"
            class="r-18jsvk2 r-4qtqp9 r-yyyyoo r-lwhw9o r-dnmrzs r-bnwqim r-1plcrui r-lrvibr r-cnnz9e"
          >
            <g>
              <path
                d="M4 4.5C4 3.12 5.119 2 6.5 2h11C18.881 2 20 3.12 20 4.5v18.44l-8-5.71-8 5.71V4.5zM6.5 4c-.276 0-.5.22-.5.5v14.56l6-4.29 6 4.29V4.5c0-.28-.224-.5-.5-.5h-11z"
              ></path>
            </g>
          </svg>
          <span>Bookmarks</span>
        </router-link>
      </div>
      <div class="nav__item">
        <router-link to="/lists">
          <svg
            viewBox="0 0 24 24"
            aria-hidden="true"
            class="r-18jsvk2 r-4qtqp9 r-yyyyoo r-lwhw9o r-dnmrzs r-bnwqim r-1plcrui r-lrvibr r-cnnz9e"
          >
            <g>
              <path
                d="M3 4.5C3 3.12 4.12 2 5.5 2h13C19.88 2 21 3.12 21 4.5v15c0 1.38-1.12 2.5-2.5 2.5h-13C4.12 22 3 20.88 3 19.5v-15zM5.5 4c-.28 0-.5.22-.5.5v15c0 .28.22.5.5.5h13c.28 0 .5-.22.5-.5v-15c0-.28-.22-.5-.5-.5h-13zM16 10H8V8h8v2zm-8 2h8v2H8v-2z"
              ></path>
            </g>
          </svg>
          <span>Lists</span>
        </router-link>
      </div>
    </nav>
  </aside>
</template>
<script>
export default {
  props: ["dark"],
  data() {
    return {};
  },
  methods: {},
};
</script>
<style scoped>
aside {
  width: 320px;
  padding: 10px 30px;
  position: fixed;
  top: 65px;
  left: 0;
  z-index: 0;
  height: 100vh;
  border-right: 1px solid rgb(245, 245, 245);
}

aside.dark {
  background: #000;
}

aside .nav .nav__item a {
  display: flex;
  align-items: center;
  border-radius: 50px;
  padding: 12px 30px 12px 15px;
  font-size: 16px;
  width: fit-content;
  font-weight: 300;
  color: rgb(25, 25, 25);
}

aside.dark .nav .nav__item a {
  color: #fff;
}

aside .nav .nav__item a:hover {
  background: rgb(240, 240, 240);
}

aside .nav .nav__item a svg {
  width: 27.5px;
  margin-right: 17.5px;
  fill: rgb(25, 25, 25);
}

aside.dark .nav .nav__item a svg {
  fill: #fff;
}

aside .nav .nav__item a.router-link-exact-active.router-link-active {
  pointer-events: none;
  font-weight: 600;
  font-size: 18px;
  cursor: auto;
}
</style>
