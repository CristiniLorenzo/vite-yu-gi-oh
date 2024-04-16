<script>
import { store } from '../store.js';
import CardCard from './CardCard.vue'

export default {
    name: 'AppMain',
    components: {
        CardCard
    },
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <main>
        

        <div class="container">

            <div class="card-container">
                <div class="cards-card">
                    <CardCard v-for="card in store.cards" :key="card.id" :cardInfo="card"></CardCard>

                </div>
            </div>
        </div>
    </main>
</template>

<style scoped lang="scss">
@use '../style/generics.scss';

main{
    width: 100%;

        .container{
            .card-container{
                width: 90%;
                margin: 0 auto;
                padding: 20px 0;
            }

            .cards-card{
                display: flex;
                flex-wrap: wrap;
                justify-content: space-between;
            }
    }
}

</style>