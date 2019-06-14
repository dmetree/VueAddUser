<template>
  <div class="container">
      <app-add-user @userAdded="newUser"></app-add-user>
      <!-- Listen to userAdded and do new method: newUser -->
      <app-user-list :users="users" @userDeleted="deleteUser"></app-user-list>
      <!-- @userDeleted is taken from UserList.vue -->
  </div>
</template>

<script>
  import User from './components/User.vue';
  import UserList from './components/UserList.vue';
  import AddUser from './components/AddUser';

  export default {
    data: function (){
      return {
        users: [
          'Ivan'
        ],
        maxUsers: 10
      }
    },
    methods: {
      // user is imported from AddUser here
      newUser(user){
        this.users.push(user);
      },
      deleteUser(index){
        this.users.splice(index, 1);
      }
    },
    
    components: {
      appUser: User,
      appUserList: UserList,
      appAddUser: AddUser
    }
}
</script>




<style>


</style>
