<template>
    <ion-page>
        <base-layout :page-title="loadMemory ? loadMemory.title : 'loiding'" default-back-link="/">
        <h1 v-if="!loadMemory">Could not Be loadind</h1>
        <memory-over-view v-else  :memory="loadMemory"></memory-over-view>

        </base-layout>
    </ion-page>
</template>

<script>
import {
    IonPage,
  
    } from '@ionic/vue'
import MemoryOverView from '../components/memories/MemoryOverView.vue';

export default {
    components:{
        IonPage,
        MemoryOverView,

    },
    data(){
        return {
            memoryId : this.$route.params.id,
        }
    },
    mounted(){
        this.memoryId = this.$route.params.id;
    },
    computed:{
        loadMemory(){
            return this.$store.getters.memory(this.memoryId);
        }
    }
}
</script>