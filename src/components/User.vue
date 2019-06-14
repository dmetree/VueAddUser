
<template>
    <div class="row">
        <div class="user">
            <slot></slot>
        </div>
       
    </div>
</template>


<script>
export default {

}
</script>

<style>
    .user{
        border: 1px solid brown;
        padding: 10px 20px;
        font-size: 20px;
        cursor: pointer;
    }

    .user:hover{
        background-color: coral;
    }
</style>
