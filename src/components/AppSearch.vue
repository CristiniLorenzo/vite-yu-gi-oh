<script>
import { store } from '../store.js';

export default {
    name: 'AppSearch',
    data(){
        return{
            store,
        }
    }
    
}
</script>

<template>
    <div class="container">
        <select v-model="store.searchedArchetype" @change="$emit('searchDone')">
            <option value="">Scegli un archetipo</option>
            <option v-for="archetype in store.archetypes" :value="archetype.archetype_name">{{ archetype.archetype_name }}</option>
        </select>
    </div>
    

</template>

<style scoped lang="scss">
    
</style>