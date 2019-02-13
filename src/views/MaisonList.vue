<template>
    <div> 
        <h1>Hello</h1>
        <div class="container">
            <div class="row">
                
                    <div v-bind:key="maison.id" v-for="maison in maisons"> 
                        
                        <Maison v-bind:maison="maison" />
                        
                        
                    </div>
                    <Maison />
                
            </div>
        </div>
        
    </div>
</template>

<script>
import Maison from '@/components/Maison.vue'
import uuid from 'uuid'
export default {
    name : 'List',
    components : {
        Maison
    },
    data() {
        return {
            maisons : [
            {
                id : 1,
                adresse : 'El Manar El Hank',
                description : 'asdsa',
                prix :'asd',
                superficie : 'asd',
                nbPieces : 'asd',
                type : 'asds'
            },
            {
                id : 2,
                adresse : 'asd',
                description : 'asdsa',
                prix :'asd',
                superficie : 'asd',
                nbPieces : 'asd',
                type : 'asds'
            }
        ]

        }
        
    }
}
</script>

<style>

</style>
