<template>
  <div class="form_wrapper">
    <form class="form_container">
      <p class="form_header">New employee</p>
      <hr />
      <div class="field">
        <label for="name">Name:</label>
        <input
          v-model="name"
          @keydown.enter="add"
          id="name"
          type="text"
          name="name"
        />
      </div>
      <div class="field">
        <label for="team">Team:</label>
        <input
          v-model="team"
          @keydown.enter="add"
          id="team"
          type="text"
          name="team"
        />
      </div>
      <div class="field">
        <label for="role">Role:</label>
        <input
          v-model="role"
          @keydown.enter="add"
          id="role"
          type="text"
          name="role"
        />
      </div>
      <div class="field">
        <label for="gmail"> Gmail </label>
        <input
          v-model="gmail"
          @keydown.enter="add"
          id="gmail"
          type="text"
          name="gmail"
        />
      </div>
      <div class="field">
        <label for="birthday">Birthday:</label>
        <input
          v-model="birthday"
          @keydown.enter="add"
          id="birthday"
          type="text"
          name="birthday"
        />
      </div>
      <div class="field">
        <label for="telegram">Telegram:</label>
        <input
          v-model="telegram"
          @keydown.enter="add"
          id="telegram"
          type="text"
          name="telegram"
        />
      </div>
      <div class="field">
        <label for="lastLogin">Last login:</label>
        <input
          v-model="lastLogin"
          @keydown.enter="add"
          id="lastLogin"
          type="text"
          name="lastLogin"
        />
      </div>
      <div class="field">
        <label for="userPermision">User Permision:</label>
        <input
          v-model="userPermision"
          @keydown.enter="add"
          id="userPermision"
          type="text"
          name="userPermision"
        />
      </div>
      <hr />
      <div class="add_buttons">
        <button @click="cleanForm" class="me-2">Cancel</button>
        <button
          @click="add"
          type="button"
        >
          Add User
        </button>
      </div>
    </form>
  </div>
</template>
<script>
export default {
  data() {
    return {
      name: "",
      team: "",
      role: "",
      gmail: "",
      birthday: "",
      telegram: "",
      lastLogin: "",
      userPermision: "",
    };
  },

  methods: {
    add() {
      const newUser = {
        name: this.name,
        team: this.team,
        role: this.role,
        gmail: this.gmail,
        birthday: this.birthday,
        telegram: this.telegram,
        lastLogin: this.lastLogin,
        userPermision: this.userPermision,
      };

      this.$emit("add-employee", newUser);
    },

    cleanForm() {
      this.name = "";
      this.team = "";
      this.role = "";
      this.gmail = "";
      this.birthday = "";
      this.telegram = "";
      this.lastLogin = "";
      this.userPermision = "";

      this.showForm = false;
    },
  },
};
</script>
