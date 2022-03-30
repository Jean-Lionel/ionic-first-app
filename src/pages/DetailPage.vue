<template>
    <ion-page>
        <base-layout :page-title="loadMemory ? loadMemory.title : 'loiding'" default-back-link="/">   
        <ion-card v-if="loadMemory">
        <ion-img :src="loadMemory.image"></ion-img>
        <ion-card-content>
            <ion-card-header>
            <ion-card-subtitle>{{loadMemory.id}}</ion-card-subtitle>
            <ion-card-title>{{loadMemory.title}}</ion-card-title>
            </ion-card-header>
            <p>
                {{loadMemory.body}}
            </p>
            <ion-item>
            <ion-button fill="solid">Action</ion-button>
            <ion-icon name="heart" slot="end"></ion-icon>
            <ion-icon name="share" slot="end"></ion-icon>
            </ion-item>
        </ion-card-content>
        </ion-card>
        <h1 v-else>Could not Be loadind</h1>

        </base-layout>
    </ion-page>
</template>

<script>
import {
    IonPage,
    IonCard,
    IonImg,
    IonCardContent,
    IonCardHeader,
    IonCardTitle,
    IonCardSubtitle,
    IonButton,
    IonItem,
    IonIcon,
    } from '@ionic/vue'

export default {
    components:{
        IonPage,
        IonCard,
        IonImg,
        IonItem,
        IonCardHeader,
        IonCardContent,
        IonCardTitle,
        IonCardSubtitle,
        IonButton,
        IonIcon
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