<script>
export default {
    name: 'AppHeader'
}
</script>

<template>
    <div class="title">
        <img src="../assets/logo.jpg" alt="">
        <h1>Yu-Gi-Oh Api</h1>
    </div>
</template>

<style scoped lang="scss">
@use '../style/generics.scss';

.title{
    display: flex;
    padding: 10px;
    background-color: white;
    margin-bottom: 50px;

        img{
            width: 100px;
        }
        h1{
            padding-left: 20px;
        }
}

</style>