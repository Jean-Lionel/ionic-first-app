<template>
        <ion-page>
            <base-layout page-title="All Memories">
                <template v-slot:actions-end>
                    <ion-button router-link="/memories/add">
                       <ion-icon slot="icon-only" :icon="add"></ion-icon>
                    </ion-button>
                </template>
               <memories-liste :memories="memories" /> 
            </base-layout>
        </ion-page>
       
</template>

<script>
import {IonPage, IonButton, IonIcon} from "@ionic/vue";
import {add} from "ionicons/icons"
import MemoriesListe from '../components/memories/MemoriesListe.vue';

export default {
    components:{
        IonPage,
        IonButton,
        IonIcon,
        MemoriesListe,

    },
    data(){
        return { 
            add
        }
    },
    computed:{
        memories(){
            return this.$store.getters.memories
        }

    }  
}
</script>