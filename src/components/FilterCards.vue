<script>
import axios from 'axios';
import { store } from '../store'

export default {
    name: 'FilterCards',
    data() {
        return {
            store
        }
    },
    created() {
        axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php').then((res) => {
            store.arrayArchetype = res.data

            console.log(store.arrayArchetype)
        })
    }
}
</script>

<template>
    <div class="debug text-center padd-10" style="background-color: orange;">
        <select name="filter-cards" id="select-cards" v-model="store.valueArchetype" @change="$emit
            ('nomeEmit')">
            <option :value="elem.archetype_name" v-for="(elem, index) in store.arrayArchetype" :key="index">
                {{ elem.archetype_name }}
            </option>
        </select>
    </div>
</template>

<style lang="scss"></style>
