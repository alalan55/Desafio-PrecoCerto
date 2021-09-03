<template>
    <div class="user-nav">
        <div class="bell">
            <i class="fas fa-bell"></i>
        </div>
        <div class="name">
            <span>teste@teste.com</span>
            <i class="fas fa-user-circle"></i>
        </div>

    </div>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>

$user-color: #999FA4;
.user-nav{
    color: white;
    display: flex;
    align-items: center;
    justify-content: space-evenly;

    .name{
        display: flex;
        align-items: center;
        justify-content: space-between;

        span{
            display: block;
            margin-right: .2rem;
            font-weight: 500;
        }

        i{
            color: $user-color;
            font-size: 30px;
        }
    }
}
</style>