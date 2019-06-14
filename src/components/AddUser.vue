<template>
    <div class="row">
       <input class="u-input" type="text" v-model="user">
       <button class="u-input-btn" @click.prevent="createNew">Add User</button>
    </div>  
</template>

<script>
    export default {
       data: function(){
           return {
               user: ''
            //    this one is set when user types smt in the input 
           };
       },
       methods: {
           createNew(){
               this.$emit('userAdded', this.user);
               this.user = '';
           }
       }
    }
</script>

<style>
    .u-input{
        border: 1px solid brown;
        padding: 10px 20px;
        font-size: 20px;
    }

    .u-input-btn{
        font-size: 20px;
        padding: 10px 20px;
        color: white;
        background: darkgreen;
    }
</style>

