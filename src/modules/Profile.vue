<template>
  <div class="profile">
    <div class="top">
      <img src="../assets/img/top.png" alt="" />
      <div class="edit">
        <div class="avatar">
          <img src="../assets/img/avatar.jpg" alt="" />
        </div>
        <div class="button">
          <button @click="$emit('toggle-modal')">Edit Profile</button>
        </div>
      </div>
    </div>
    <div class="user">
      <div class="user-name">{{ profile.userName }}</div>
      <div class="user-email">{{ profile.userEmail }}</div>
    </div>
    <div class="bio">
      {{ profile.bio }}
    </div>
    <div class="private">
      <div class="private-item">
        <svg
          viewBox="0 0 24 24"
          aria-hidden="true"
          class="r-14j79pv r-4qtqp9 r-yyyyoo r-1xvli5t r-1d4mawv r-dnmrzs r-bnwqim r-1plcrui r-lrvibr"
        >
          <g>
            <path
              d="M12 7c-1.93 0-3.5 1.57-3.5 3.5S10.07 14 12 14s3.5-1.57 3.5-3.5S13.93 7 12 7zm0 5c-.827 0-1.5-.673-1.5-1.5S11.173 9 12 9s1.5.673 1.5 1.5S12.827 12 12 12zm0-10c-4.687 0-8.5 3.813-8.5 8.5 0 5.967 7.621 11.116 7.945 11.332l.555.37.555-.37c.324-.216 7.945-5.365 7.945-11.332C20.5 5.813 16.687 2 12 2zm0 17.77c-1.665-1.241-6.5-5.196-6.5-9.27C5.5 6.916 8.416 4 12 4s6.5 2.916 6.5 6.5c0 4.073-4.835 8.028-6.5 9.27z"
            ></path>
          </g>
        </svg>
        <span>{{ profile.address }}</span>
      </div>
      <div class="private-item">
        <svg
          viewBox="0 0 24 24"
          aria-hidden="true"
          class="r-14j79pv r-4qtqp9 r-yyyyoo r-1xvli5t r-1d4mawv r-dnmrzs r-bnwqim r-1plcrui r-lrvibr"
        >
          <g>
            <path
              d="M7 4V3h2v1h6V3h2v1h1.5C19.89 4 21 5.12 21 6.5v12c0 1.38-1.11 2.5-2.5 2.5h-13C4.12 21 3 19.88 3 18.5v-12C3 5.12 4.12 4 5.5 4H7zm0 2H5.5c-.27 0-.5.22-.5.5v12c0 .28.23.5.5.5h13c.28 0 .5-.22.5-.5v-12c0-.28-.22-.5-.5-.5H17v1h-2V6H9v1H7V6zm0 6h2v-2H7v2zm0 4h2v-2H7v2zm4-4h2v-2h-2v2zm0 4h2v-2h-2v2zm4-4h2v-2h-2v2z"
            ></path>
          </g>
        </svg>
        <span>Registered at August 2022</span>
      </div>
    </div>
    <div class="follow">
      <div class="follow-item">{{ profile.followers }}-Followers</div>
      <div class="follow-item">{{ profile.following }}-Following</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Profile",
  props: {
    profile: {
      type: Object,
      required: true,
    },
  },
  data() {
    return {};
  },
  methods: {},
};
</script>

<style scoped>
.profile {
  border-right: 1px solid rgb(245, 245, 245);
}

.profile .top img {
  width: 100%;
  height: 185px;
}

.profile .top .edit {
  display: flex;
  justify-content: space-between;
  position: relative;
  padding: 5px 25px;
}

.profile .top .edit .avatar img {
  width: 145px;
  height: 145px;
  border-radius: 100%;
  left: 0;
  top: 0;
  transform: translate(10%, -50%);
  border: 3px solid #fff;
  position: absolute;
}

.profile .top .edit .button button {
  padding: 7.5px 25px;
  border-radius: 30px;
  border: 1px solid rgb(225, 225, 225);
  font-size: 15px;
}

.profile .top .edit .button button:hover {
  background: rgb(245, 245, 245);
}

.profile .user {
  margin-top: 40px;
  padding: 5px 25px 15px;
  border-bottom: 1px solid rgb(245, 245, 245);
}

.profile .user-name {
  font-size: 20px;
  font-weight: 600;
}

.profile .user-email {
  font-size: 15px;
  font-weight: 300;
  color: rgb(150, 150, 150);
}

.profile .bio {
  font-size: 14px;
  padding: 15px 25px 5px;
}

.profile .private {
  padding: 10px 25px;
  display: flex;
}

.profile .private-item {
  display: flex;
  align-items: center;
  margin-right: 15px;
}

.profile .private-item svg {
  width: 20px;
  fill: rgb(150, 150, 150);
  margin-right: 5px;
}

.profile .private-item span {
  color: rgb(150, 150, 150);
  font-size: 14px;
  font-weight: 600;
}

.follow {
  display: flex;
  padding: 10px 25px;
}

.follow-item {
  margin-right: 15px;
  font-size: 14px;
  font-weight: 600;
}
</style>
