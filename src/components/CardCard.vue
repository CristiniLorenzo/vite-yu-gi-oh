<script>
export default {
    name: 'CardCard',
    props: {
        cardInfo: Object
    }
}
</script>

<template>
    <div class="card-card">
        <div class="image" v-for="image in cardInfo.card_images">
            <img :src="image.image_url_small" alt="">
        </div>
        <div class="cards-info">
            <h3>{{cardInfo.name}}</h3>
            <div>{{ cardInfo.archetype }}</div>
        </div>
    </div>


</template>

<style scoped lang="scss">
.card-card{
    width: calc((100% / 5) - 10px);
    background-color: #D48F38;
    text-align: center;
        img{
            width: 100%;
        }
        .cards-info{
            height: 110px;

            h3{
            color: white;
            }
        }
    
    
    
}
</style>