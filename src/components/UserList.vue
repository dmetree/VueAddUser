<template>
    <div class="list-row">
        <app-user v-for="(user, index) in users" @click.native="deleteUser(index)">{{ user }}</app-user>
    </div>
</template>


<script>
    import User from './User.vue';
    export default {
        
        props: ['users'],
        components: {
            appUser: User
        },
        methods: {
            deleteUser(index){
                this.$emit('userDeleted', index);
            }
        }
    }
</script>

<style>
    .list-row{
        padding: 5px 0;
        background-color: ivory;
    }
</style>

