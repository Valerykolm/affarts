<template>
  <div class="container">
    <div class="row">
      <div class="col">Menu</div>
      <div class="col">Login</div>
    </div>
    <div class="row-auto user_table">
      <div class="col-md-auto">
        <table class="table">
          <thead id="thead">
            <tr>
              <th scope="col">Business Name</th>
              <th scope="col">Team</th>
              <th scope="col">Role</th>
              <th scope="col">Gmail</th>
              <th scope="col">Birthday</th>
              <th scope="col">Telegram</th>
              <th scope="col">Last login</th>
              <th scope="col">User permision</th>
            </tr>
          </thead>
          <tbody>
            <tr
              v-for="user in users"
              v-bind:key="user.name"
              class="text-center"
            >
              <td>{{ user.name }}</td>
              <td>{{ user.team }}</td>
              <td>{{ user.role }}</td>
              <td>{{ user.gmail }}</td>
              <td>{{ user.birthday }}</td>
              <td>{{ user.telegram }}</td>
              <td>{{ user.lastLogin }}</td>
              <td><a 
                  @click="selectedUser = user" 
                  href="#"
                >
                  Edit
                </a>
                <a @click="handleDelete(user)" href="#">Delete</a>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>   
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      number: 1,
      selectedUser: null,
      users: [
        {name: 'Sarah Conor', team: 'Crosty', role: 'TeamLead', gmail: 'sarahconnor@gmail.com', birthday: '25.04.1994', telegram: '@sarahconnor', lastLogin: '03.11.2021', userPermision: ''},
        {name: 'Sarah Conor', team: 'Crosty', role: 'TeamLead', gmail: 'sarahconnor@gmail.com', birthday: '25.04.1994', telegram: '@sarahconnor', lastLogin: '03.11.2021', userPermision: ''},
        {name: 'Sarah Conor', team: 'Crosty', role: 'TeamLead', gmail: 'sarahconnor@gmail.com', birthday: '25.04.1994', telegram: '@sarahconnor', lastLogin: '03.11.2021', userPermision: ''}
      ]
    }
  },
  methods: {
    handleDelete(userToRemove) {
      this.user = this.users.filter(u => u !== userToRemove);
    },
  }
}
</script>
<style src="./assets/bootstrap.min.css"></style>
