<template>
  <section :class="{ dark: dark }">
    <Profile @toggle-modal="openModal = !openModal" :profile="profile" />
    <Modal
      :dark="dark"
      title="Edit Profile"
      v-show="openModal"
      @toggle-modal="openModal = !openModal"
      @save-profile-modal="saveProfileModal"
    >
      <ProfileModal :dark="dark" :profileForm="profileForm" />
    </Modal>
    <div class="bar"></div>
  </section>
</template>
<script>
import Modal from "../components/Modal.vue";
import ProfileModal from "../modals/ProfileModal.vue";
import Profile from "../modules/Profile.vue";

export default {
  name: "Home",
  props: ["dark"],
  data() {
    return {
      openModal: true,
      profile: {
        userName: "Temurmalik Abduqodirov",
        userEmail: "temurmalikreact@gmail.com",
        bio: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Modi impedit, atque, consectetur earum eaque aliquam eius reiciendis ea at quia repellat cupiditate necessitatibus saepe voluptates quis, eveniet recusandae dolores veritatis.",
        address: "Ferghana, Uzbekistan",
        followers: 0,
        following: 5,
      },
      profileForm: {
        userName: "",
        userEmail: "",
        bio: "",
        address: "",
        followers: 0,
        following: 0,
      },
    };
  },
  components: {
    Modal,
    ProfileModal,
    Profile,
  },
  mounted() {
    this.profileForm = JSON.parse(JSON.stringify(this.profile));
  },
  methods: {
    saveProfileModal() {
      this.profile = JSON.parse(JSON.stringify(this.profileForm));
      this.openModal = !this.openModal;
    },
  },
};
</script>
<style scoped>
section {
  margin: 65px 0 0 320px;
  display: grid;
  grid-template-columns: 7fr 5fr;
  min-height: 100vh;
}

section.dark {
  background: #000;
  color: #fff;
}
</style>
