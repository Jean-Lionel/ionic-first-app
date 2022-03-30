<template>
        <ion-page>
            <base-layout page-title="All Memories">
               <memories-liste :memories="memories" /> 
            </base-layout>
        </ion-page>
       
</template>

<script>
import {IonPage} from "@ionic/vue";
import MemoriesListe from '../components/memories/MemoriesListe.vue';

export default {
    components:{
        IonPage,
        MemoriesListe,

    },
    data(){
        return {     }
    },
    computed:{
        memories(){
            return this.$store.getters.memories
        }

    }  
}
</script>