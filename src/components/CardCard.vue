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
        <div class="image">
            <img src="https://images.ygoprodeck.com/images/cards_small/34541863.jpg" alt="">
        </div>
        <div class="cards-info">
            <h3>nome della carta</h3>
            <div>specie delle carta</div>
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