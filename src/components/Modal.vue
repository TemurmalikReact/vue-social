<template>
  <div>
    <div class="modal" :class="{ dark: dark }">
      <div class="modal-header">
        <button @click="$emit('toggle-modal')" class="modal-close">
          <svg
            viewBox="0 0 24 24"
            aria-hidden="true"
            class="r-18jsvk2 r-4qtqp9 r-yyyyoo r-z80fyv r-dnmrzs r-bnwqim r-1plcrui r-lrvibr r-19wmn03"
          >
            <g>
              <path
                d="M10.59 12L4.54 5.96l1.42-1.42L12 10.59l6.04-6.05 1.42 1.42L13.41 12l6.05 6.04-1.42 1.42L12 13.41l-6.04 6.05-1.42-1.42L10.59 12z"
              ></path>
            </g>
          </svg>
        </button>
        <div class="modal-title">
          {{ title }}
        </div>
        <button @click="$emit('save-profile-modal')" class="modal-save">
          Save
        </button>
      </div>
      <div class="slot">
        <slot></slot>
      </div>
    </div>
    <div @click="$emit('toggle-modal')" class="background"></div>
  </div>
</template>
<script>
export default {
  name: "Modal",
  props: {
    title: String,
    dark: Boolean,
  },
  data() {
    return {
      activeColor: "white",
      colors: ["white", "green", "blue"],
    };
  },
};
</script>

<style scoped>
.modal {
  position: fixed;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  z-index: 15;
  width: 44%;
  height: 90vh;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  background: #fff;
}

.modal.dark {
  background: #000;
  color: #fff;
}

.modal-header {
  display: flex;
  align-items: center;
  width: 100%;
  justify-content: space-between;
  padding: 10px 10px 10px 10px;
}

.modal-close {
  background: none;
  border: none;
}

.modal-close svg {
  width: 25px;
}

.modal.dark .modal-close svg {
  fill: #fff;
}

.modal-title {
  font-size: 25px;
  font-weight: 600;
}

.modal-save {
  border: none;
  background: rgba(50, 50, 50);
  color: #fff;
  border-radius: 50px;
  padding: 5px 15px;
  font-size: 15px;
}

.slot {
  margin-top: 5px;
  overflow-y: scroll;
  flex: 1;
  position: relative;
  z-index: 10;
}

.background {
  position: fixed;
  left: 0;
  top: 0;
  z-index: 5;
  width: 100%;
  height: 100%;
  background: rgba(50, 50, 50, 0.75);
}
</style>
