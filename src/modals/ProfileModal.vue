<template>
  <div class="profile-modal">
    <div class="top">
      <img src="../assets/img/top.png" alt="" />
      <div class="edit">
        <div class="avatar">
          <img src="../assets/img/avatar.jpg" alt="" />
        </div>
      </div>
    </div>
    <div class="profile-modal-wrapper">
      <div class="profile-modal-item">
        <label>
          <span>Name</span>
          <input
            :class="{ dark: dark }"
            type="text"
            v-model="profileForm.userName"
          />
        </label>
      </div>
      <div class="profile-modal-item">
        <label>
          <span>Email</span>
          <input
            :class="{ dark: dark }"
            type="text"
            v-model="profileForm.userEmail"
          />
        </label>
      </div>
      <div class="profile-modal-item">
        <label>
          <span>Bio</span>
          <textarea :class="{ dark: dark }" v-model="profileForm.bio">
          </textarea>
        </label>
      </div>
      <div class="profile-modal-item">
        <label>
          <span>Adress</span>
          <input
            :class="{ dark: dark }"
            type="text"
            v-model="profileForm.address"
          />
        </label>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProfileModal",
  props: {
    profileForm: {
      type: Object,
      required: true,
    },
    dark: Boolean,
  },
  data() {
    return {};
  },
  methods: {},
};
</script>

<style scoped>
.profile-modal .profile-modal-wrapper {
  margin-top: 65px;
}

.profile-modal .profile-modal-wrapper .profile-modal-item {
  padding: 5px 20px;
  width: 100%;
}

.profile-modal .profile-modal-wrapper .profile-modal-item label {
  width: 100%;
  display: flex;
  flex-direction: column;
  margin-bottom: 15px;
  font-size: 15px;
}

.profile-modal .profile-modal-wrapper .profile-modal-item label span {
  font-weight: 600;
  margin-bottom: 3px;
}

.profile-modal .profile-modal-wrapper .profile-modal-item label textarea,
input {
  border: 2px solid rgba(0, 0, 0, 0.05);
  outline: none;
  height: 35px;
  padding: 5px 15px;
}

.profile-modal .profile-modal-wrapper .profile-modal-item label textarea.dark,
input.dark {
  border: 2px solid #fff;
  color: #fff;
}

.profile-modal .profile-modal-wrapper .profile-modal-item label textarea {
  height: 65px;
  resize: none;
}

.profile-modal
  .profile-modal-wrapper
  .profile-modal-item
  label
  textarea::-webkit-scrollbar {
  width: 0;
}

.profile-modal .top img {
  width: 100%;
  height: 185px;
}

.profile-modal .top .edit {
  display: flex;
  justify-content: space-between;
  position: relative;
  padding: 5px 25px;
}

.profile-modal .top .edit .avatar img {
  width: 125px;
  height: 125px;
  border-radius: 100%;
  left: 0;
  top: 0;
  transform: translate(10%, -50%);
  border: 3px solid #fff;
  position: absolute;
}
</style>
